# Vacation Trip Store Application

This milestone for C# I was aimed at creating a GUI application that acted as a store inventory for different vacation trips. Due to Grand Canyon University policy, code snippets are only allowed and will be the only code provided. 

#### Languages
C#

#### Frameworks
.NET

#### IDE
Visual Studio 2019


## Functionality

- Add a trip
  - Name
  - Location
  - Date
  - Price
  - Duration
  - Quantity
  - Photo URL
  - Description
- Edit a trip
- Search for a trip
- Change the quantity of a trip
- Delete a trip
- Sort trips
- Upload a file
- Save trip(s) to a file

#### Skills

- Formulate a UML class diagram
- Creation of multiple classes
- Usage of various graphical controls including text box, date time picker, buttons (GUI version)
- Passing of information between forms (GUI version)
         
## Code Snippets

### Parsing
Textbox was parsed as a float data type and saved as a float under the name of price.
```
float price = float.Parse(txt_price.Text);
```

### Constructors
Constructor was called for a new trip named t. Appropriate arguments were passed for the parameters of this constructor.
```
Trip t = new Trip(name, location, date, price, duration, description, quantity, URL);
```

### Operators
```
//Add |, so that when file is uploaded it can load properly
string oneLine = t.name + "|" + t.location + "|" + t.date + "|" + t.price + "|" +     t.duration + "|" + t.description + "|" + t.quantity + "|" + t.photoURL;
```
  
### If ... Else
This was nested in a foreach loop. The foreach iterated through an array (variable name chosen was t) and if the name was empty, a message box would print that there are no trips, else (if there were names) it would add it to the list box.
```
//If there are no trips
if (t.name.Equals(null))
  MessageBox.Show("There are no trips yet");
//Otherwise
else
  listBox1.Items.Add(t.ToString());
```

### Methods
This method is called when the delete button is clicked. It will remove a trip from the list.
```
//Remove method
remove();
```

NOTE: Only code snippets are allowed, but this is called when the delete button is clicked. It will get the selected index, confirm to the user that they would like to delete the trip, and then remove the trip from the list. Getting the index would look like this:
```
int i = listBox1.SelectedIndex;
```

### User Input
*Console Version* Will ask for a new name for the trip using `Console.WriteLine()` and save the input to a string variable using `Console.ReadLine()`.
```
Console.WriteLine("What is the new name?");
string newName = Console.ReadLine();
```
