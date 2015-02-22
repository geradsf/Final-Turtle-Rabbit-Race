# Final-Turtle-Rabbit-Race
<script>
	var Animal = function(n, s, f) {
		this.name = n;
		this.speed = s;
		this.focus= f;
		this.position = 0;
		this.report = function() {
			return this.name + " is at " + this.position;
		};
		this.run = function() {
			if(this.focus > (Math.random() * 10)) {
			this.position += this.speed;
			}
		};
	}
		
	var turtle = new Animal("Pete", 2, 8.5),
		rabbit = new Animal("Mopsy", 8, 4);
		
	var distance = 25;
	
	while(turtle.position < distance && rabbit.position < distance) {
		turtle.run();
		rabbit.run();
	};
		
	console.log(turtle.report());
	console.log(rabbit.report());
</script>
