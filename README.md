# Electric Car Class Implementation 
Enhance your understanding of inheritance in object-oriented programming by extending a Car class to create an Electric Car (EV) class. This new class will include additional properties and methods specific to electric vehicles.

// Parent class 'Car'
function Car(make, speed) {
  this.make = make;
  this.speed = speed;
  }
  
// Inheriting from 'Car'
EV.prototype = Object.create(Car.prototype);
EV.prototype.constructor = EV;

// 'chargeBattery' method
EV.prototype.chargeBattery = function(chargeTo) {
  this.charge = chargeTo;
  console.log(`${this.make} charged to ${chargeTo}%`);
};
// 'accelerate' method
EV.prototype.accelerate = function() {
  this.speed += 20;
  this.charge -= 1;
  console.log(`${this.make} going at ${this.speed} km/h with a charge of ${this.charge}%`);
};

// Test data
const tesla = new EV('Tesla', 120, 23);

// Experiment with methods
tesla.accelerate(); // Output: Tesla going at 140 km/h with a charge of 22%
tesla.chargeBattery(90); // Output: Tesla charged to 90%
tesla.accelerate(); // Output: Tesla going at 160 km/h with a charge of 89%
