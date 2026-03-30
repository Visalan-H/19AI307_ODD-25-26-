# Ex.No:4(D) DESIGN PATTERN ---- BEHAVIOUR PATTERN

## AIM:

Implement the **MVC (Model–View–Controller)** behaviour pattern where:

- **Model** stores product info
- **View** displays product details
- **Controller** updates product data and refreshes the view automatically

## ALGORITHM :

1. Create a `Product` model to store item name and price.
2. Create a `ProductView` class to display the product details.
3. Create a `ProductController` class to manage updates to the model.
4. When the controller updates the price, it triggers the view to refresh.
5. In the main program, create model, view, controller, update data, and display results.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### to implement a Behaviour Pattern using Java

## SOURCE CODE:

```java
// Model
class Product {
    private String name;
    private double price;

    Product(String name, double price) {
        this.name = name;
        this.price = price;
    }

    String getName() { return name; }
    double getPrice() { return price; }

    void setPrice(double price) {
        this.price = price;
    }
}

// View
class ProductView {
    void display(Product p) {
        System.out.println("Product: " + p.getName());
        System.out.println("Price: " + p.getPrice());
    }
}

// Controller
class ProductController {
    private Product model;
    private ProductView view;

    ProductController(Product model, ProductView view) {
        this.model = model;
        this.view = view;
    }

    void updatePrice(double newPrice) {
        model.setPrice(newPrice);
        refreshView();
    }

    void refreshView() {
        view.display(model);
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Product model = new Product("Laptop", 50000);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(model, view);

        controller.refreshView();
        controller.updatePrice(55000);
    }
}
```

## OUTPUT:

```
Product: Laptop
Price: 50000.0
Product: Laptop
Price: 55000.0
```

## RESULT:

Program executed successfully.
