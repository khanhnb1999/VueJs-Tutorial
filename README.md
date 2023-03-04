## 1: Ràng buộc dữ liệu là nội suy văn bản(text interpolation).
## 2: Sử dụng cú pháp mustache(ria mép).
    <span>Thông điệp: {{ content }}</span>.
	
## 3: v-once: Không cập nhật lại khi dữ liệu thay đổi.
## 4: v-bind:id : 
	<p v-bind:id='content'>{{ content }}</p> => <p id='content'></p>
	content: dữ liệu được ràng buộc trong data.
		
## 5: v-bind:class : Tương tự như trên, thay class=id
	
## 6: v-bind:disable: 
    <button v-bind:disable='isDisable'>Click me!!!</button>
    isDisable: Dữ liệu được ràng buộc trong data.
    true => button là disable và ngược lại.
		
## 7 
    1 directive có thể chấp nhận 1 tham số, đánh dấu bằng 1 dấu 2 chấm, theo sau là tên của directive:
    v-bind:href, v-on:click
	
## 8
    v-bind:tên thuộc tính hoặc : + tên thuộc tính =>  Thường sử dụng cho các thuộc tính trong thẻ HTML.
## 9 
    v-on:tên event hoặc @ + tên event => Thường sử dụng cho các sự kiện
	
## 10: v-bind:class or :class
	 <h1 :class="{content : isDisable, header__title : isDisable}">Learn more about</h1>