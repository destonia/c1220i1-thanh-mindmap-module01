###Reflection 14/1/2021
	Thao tác di chuyển 1 đối tượng là các bước:
	thêm đối tượng với tọa độ ban đầu
	->ẩn đối tượng->thay đội tọa độ của đối tượng
	->hiện thị lại đối tượng với tọa độ vừa thay đổi đặt trong 1 vòng lặp hoặc gọi ra bằng 1 action.
	ví dụ: 
	
	class Circle {
		constructor(x,y,radius) {
        this.x = x;
        this.y = y;
        this.radius = radius;
        this.color = "blue";
        this.direct = 'left';
    }

    setColor(color){
        this.color = color;
    }

    moveRight(){
        this.x += 5;
    }

    moveLeft(){
        this.x -= 5;
    }

    render(canvas){
        // let ctx = document.getElementById("myCanvas").getContext('2d');
        let ctx = canvas.getContext('2d');
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.radius, 0, 2 * Math.PI);
        ctx.fillStyle = this.color;
        ctx.fill();
		}
	}

	Khai báo một class bằng 

		class className{
		constructtor(){
			}
		}

	Thay vì funtion className(){}
	Để tránh nhầm lẫn giữa function và class:
		ta dùng:

		class Circle {
		constructor(x,y,radius) {
        this.x = x;
        this.y = y;
        this.radius = radius;
        this.color = "blue";
        this.direct = 'left';
    }

	thay cho:

	function Circle(x,y,radius){
	this.x=x;
	this.y=y;
	this.radius=radius;
	}
