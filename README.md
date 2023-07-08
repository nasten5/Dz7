# Dz7
public class Phone implements Comparable<Phone> {
private String manufacturer;
private String model;
private double price;

public Phone(String manufacturer, String model, double price) {
this.manufacturer = manufacturer;
this.model = model;
this.price = price;
}

public String getManufacturer() {
return manufacturer;
}

public String getModel() {
return model;
}

public double getPrice() {
return price;
}
@Override
public int compareTo(Phone other) {
return Double.compare(this.price, other.price);
}
}

ArrayList<Phone> phones = new ArrayList<>();
phones.add(new Phone("Apple", "iPhone 12", 799.99));
phones.add(new Phone("Samsung", "Galaxy S21", 699.99));
phones.add(new Phone("Google", "Pixel 5", 699.99));
phones.add(new Phone("OnePlus", "9 Pro", 969.99));
phones.stream()
.sorted()
.forEach(p -> System.out.println(p.getModel() + " - $" + p.getPrice()));
