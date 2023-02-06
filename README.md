# Serialising-class-instances
 
class Car {
 constructor(color, speed) {
 this.color = color;
 this.speed = speed;
 this.id_ = Math.random();
 }
 toJSON() {
 return {
 $type: 'com.example.Car',
 color: this.color,
 speed: this.speed
 };
 }
 static fromJSON(data) {
 return new Car(data.color, data.speed);
 }
}
var userJson = JSON.stringify({
 name: "John",
 car: new Car('red', 'fast')
});
