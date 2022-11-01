In words: How much fuel do we have left in our tank after putting in 10 gallons, and driving 40 miles?
In order to perform the chaining, the methods should return the $this keyword.
In order for us to be able to perform the chaining, the methods should return the object and, since we are inside the class, the methods should return the $this keyword. In the code below, we can see how each method returns the $this keyword in order to allow the chaining.
class Car {
public $tank;
// Add gallons of fuel to the tank when we fill it
public function fill($float)
{
$this-> tank += $float;
return $this;
}
// Subtract gallons of fuel from the tank as we ride the car
public function ride($float)
{
$miles = $float;
$gallons = $miles/50;
$this-> tank -= $gallons;
return $this;
}
}

Now, we can create an object from the Car class with the name of $bmw and find out the number of gallons of fuel left in our car’s tank after we have filled the tank with 10 gallons of fuel and driven40 miles.
// Create an object from the Car class
$bmw = new Car();
// Add 10 gallons of fuel, then ride 40 miles
// and get the number of gallons in the tank
$tank = $bmw -> fill(10) -> ride(40) -> tank;
// Print the results to the screen
echo "The number of gallons left in the tank: " . $tank . " gal.";

Result:
The number of gallons left in the tank: 9.2 gal.
