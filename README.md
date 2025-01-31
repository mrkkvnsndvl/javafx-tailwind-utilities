# Tailwind Utilities for JavaFX (CSS)

This repository contains a CSS file (`tailwind-utilities.css`) that provides a set of utility classes inspired by [Tailwind CSS](https://tailwindcss.com/) for styling JavaFX applications. These utilities are designed to make it easier to apply consistent and responsive styles to JavaFX components using a utility-first approach.

## Features

- **Color Utilities**: Includes a wide range of color classes for fills, text, and backgrounds, following the Tailwind color palette.
- **Spacing Utilities**: Provides padding and margin utilities for consistent spacing.
- **Sizing Utilities**: Includes classes for setting minimum, maximum, and preferred widths and heights.
- **Typography Utilities**: Offers font size and weight utilities for text styling.
- **Border Utilities**: Includes border radius, width, and color utilities for customizing borders.
- **Effects Utilities**: Provides shadow and opacity utilities for visual effects.
- **Interactivity Utilities**: Includes cursor utilities for better user interaction.

## Usage

To use these utilities in your JavaFX application, simply include the `tailwind-utilities.css` file in your project and apply the classes to your JavaFX components.

### Example

#### Java Example

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Main extends Application {
    @Override
    public void start(Stage primaryStage) {
        Button btn = new Button("Click Me");
        btn.getStyleClass().add("bg-blue-500"); // Apply a background color
        btn.getStyleClass().add("text-white");  // Apply white text color
        btn.getStyleClass().add("p-4");         // Apply padding

        StackPane root = new StackPane();
        root.getChildren().add(btn);

        Scene scene = new Scene(root, 300, 200);
        scene.getStylesheets().add(getClass().getResource("tailwind-utilities.css").toExternalForm());

        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

#### FXML Example

If you're using FXML for your layout, you can include the CSS file in your FXML file like this:

```xml
<?import javafx.scene.layout.StackPane?>
<?import javafx.scene.control.Button?>

<StackPane xmlns:fx="http://javafx.com/fxml" fx:controller="your.controller.Class">
    <stylesheets>
        <URL value="@tailwind-utilities.css" />
    </stylesheets>
    
    <Button text="Click Me" styleClass="bg-blue-500 text-white p-4"/>
</StackPane>
```

In Scene Builder:
1. Open your FXML file in Scene Builder.
2. In the **Preview** tab, navigate to **Scene Style Sheets**.
3. Click **Add** and choose the `tailwind-utilities.css` file to apply the styles.

## Installation

To use the `tailwind-utilities.css` in your project, make sure that the CSS file is placed in the correct directory. If you're using Maven or Gradle, ensure the file is in the appropriate resources folder. You can then reference it in your Java or FXML code as demonstrated above.
