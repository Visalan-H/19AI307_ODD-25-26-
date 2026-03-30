# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## AIM:

Create UI components (Buttons and TextFields) using the Abstract Factory Pattern so the program can switch between Light and Dark themes without changing component-creation code.

## ALGORITHM :

1. Define abstract product interfaces for UI elements.
2. Create concrete Light and Dark versions of each product.
3. Create an abstract factory declaring methods for creating UI components.
4. Implement LightThemeFactory and DarkThemeFactory to return theme-specific components.
5. Select a factory in the main class and use it to create themed UI components.

#### Developed By: Visalan H

#### Register Number: 212223240183

## PROGRAM:

### implement a Abstract Factory Pattern using Java

## SOURCE CODE:

```java
// Product Interfaces
interface Button {
    void render();
}

interface TextField {
    void render();
}

// Light Theme Products
class LightButton implements Button {
    public void render() {
        System.out.println("Rendering Light Button");
    }
}

class LightTextField implements TextField {
    public void render() {
        System.out.println("Rendering Light TextField");
    }
}

// Dark Theme Products
class DarkButton implements Button {
    public void render() {
        System.out.println("Rendering Dark Button");
    }
}

class DarkTextField implements TextField {
    public void render() {
        System.out.println("Rendering Dark TextField");
    }
}

// Abstract Factory
interface ThemeFactory {
    Button createButton();
    TextField createTextField();
}

// Light Theme Factory
class LightThemeFactory implements ThemeFactory {
    public Button createButton() {
        return new LightButton();
    }
    public TextField createTextField() {
        return new LightTextField();
    }
}

// Dark Theme Factory
class DarkThemeFactory implements ThemeFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public TextField createTextField() {
        return new DarkTextField();
    }
}

// Factory Selector
class ThemeFactoryProducer {
    static ThemeFactory getFactory(String type) {
        if (type.equalsIgnoreCase("light")) {
            return new LightThemeFactory();
        } else if (type.equalsIgnoreCase("dark")) {
            return new DarkThemeFactory();
        }
        return null;
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {

        ThemeFactory lightFactory = ThemeFactoryProducer.getFactory("light");
        Button lightBtn = lightFactory.createButton();
        TextField lightTxt = lightFactory.createTextField();

        lightBtn.render();
        lightTxt.render();

        ThemeFactory darkFactory = ThemeFactoryProducer.getFactory("dark");
        Button darkBtn = darkFactory.createButton();
        TextField darkTxt = darkFactory.createTextField();

        darkBtn.render();
        darkTxt.render();
    }
}
```

## OUTPUT:

```
Rendering Light Button
Rendering Light TextField
Rendering Dark Button
Rendering Dark TextField
```

## RESULT:

Program executed successfully.
