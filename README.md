## 1: Ràng buộc dữ liệu là nội suy văn bản(text interpolation).
## 2: Sử dụng cú pháp mustache(ria mép).
    <span>Thông điệp: {{ content }}</span>.
      + v-once: Không cập nhật lại khi dữ liệu thay đổi.
## 4: v-bind:id và v-bind:class
	 <p v-bind:id='content'>{{ content }}</p> => <p id='content'></p>.
	 + content: dữ liệu được ràng buộc trong data.
    + v-bind:class : Tương tự như trên, thay class=id
    + <h1 :class="{content : isDisable, header__title : isDisable}">Learn more about</h1>
## 6: v-bind:disable: 
     <button v-bind:disable='isDisable'>Click me!!!</button>
    + isDisable: Dữ liệu được ràng buộc trong data.
    + true => button là disable và ngược lại.
    + 1 directive có thể chấp nhận 1 tham số, đánh dấu bằng 1 dấu 2 chấm, theo sau là tên của directive:
    + v-bind:href, v-on:click
    + v-bind:tên thuộc tính hoặc : + tên thuộc tính =>  Thường sử dụng cho các thuộc tính trong thẻ HTML.
    + v-on:tên event hoặc @ + tên event => Thường sử dụng cho các sự kiện
## 7: Cách sử dụng class cho các trường hợp khác nhau    
      Component: <HelloWord class="content" />
    + Phần tử HTML nằm trong component <HelloWord /> sẽ được thêm vào class="content"
    + VD: <h3 class="title">Toi di code dao</h3> => <h3 class="title content">Toi di code dao</h3>
## 8: Render theo điều kiện
    v-if:
    + <h1 v-if="ok">Mọi việc ổn cả</h1>
    + <h1 v-else>Có gì đó sai sai</h1>      
    + Để v-else hợp lệ thì nó phải theo sau phần tử v-if

    v-else-if:
    + <div v-if="type === 'A'">A</div>
    + <div v-else-if="type === 'B'">B</div>
    + <div v-else-if="type === 'C'">C</div>
    + <div v-else-if="type === 'D'">D</div>
    + <div v-else>Chiến Sĩ không thể nhớ nổi</div>

    v-show: Tương tự v-if
    + <h1 v-show="ok">Xin chào!</h1>

    Điểm khác biệt:
    + v-show: Luôn hiện thị trong DOM mặc dù điều kiện đó là true/false, chỉ hiện/giấu đi dựa vào css.
    + v-if: Nếu điều kiện là false thì lần render đầu tiên nó ko hiện thị vào DOM.