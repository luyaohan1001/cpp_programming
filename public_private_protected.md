### Here's a note to help under what these three keywords means and how they are used.

| Modifier     | Data Protection                                   |
|:-------------|:--------------------------------------------------|
| public       | Any class can access						       | 
| protected    | Only child / friend can access                    |
| private      | Only itself / friend can access (not even child!) |

Example:
	class Car {
		public:
			int color;
		protected:
			int mileage;
		private:
			int speed;
	};
	
	class raceCar : public Car {
		// color is public
		// mileage is protected
		// speed is not inherited, not there for child.
	};
	
	class raceCar : protected Car {
		// color is protected
		// mileage is protected
		// speed is not inherited, not there for child.
	};
	
	class raceCar : private Car {
		// color is private
		// mileage is private
		// speed is not inherited, not there for child.
	};
