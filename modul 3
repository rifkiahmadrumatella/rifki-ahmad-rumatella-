 import javafx.application.Application;
 import javafx.scene.Scene;
 import javafx.scene.control.*;
 import javafx.scene.layout.*;
 import javafx.stage.Stage;
 public class LoginApp extends Application {
    private static final String CORRECT_USERNAME = "admin";
    private static final String CORRECT_PASSWORD = "password";

    private Stage primaryStage;
    private BorderPane loginPane;
    private BorderPane mainPane;

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        this.primaryStage = primaryStage;
        setupLoginPane();
        setupMainPane();

        Scene scene = new Scene(loginPane, 400, 300);
        primaryStage.setTitle("Login App");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    private void setupLoginPane() {
        loginPane = new BorderPane();
        VBox loginBox = new VBox(10);
        loginBox.setPadding(new Insets(20));

        Label titleLabel = new Label("Login");
        titleLabel.setStyle("-fx-font-size: 18px; -fx-font-weight: bold;");
        TextField usernameField = new TextField();
        PasswordField passwordField = new PasswordField();
        Button loginButton = new Button("Login");

        loginButton.setOnAction(e -> {
            String username = usernameField.getText();
            String password = passwordField.getText();

            if (username.equals(CORRECT_USERNAME) && password.equals(CORRECT_PASSWORD)) {
                showMainPage();
            } else {
                showAlert("Username or password is incorrect.");
            }
        });

        loginBox.getChildren().addAll(titleLabel, new Label("Username:"), usernameField,
                new Label("Password:"), passwordField, loginButton);
        loginPane.setCenter(loginBox);
    }

    private void setupMainPane() {
        mainPane = new BorderPane();
        Label welcomeLabel = new Label("Welcome to the Main Page!");
        welcomeLabel.setStyle("-fx-font-size: 18px; -fx-font-weight: bold;");
        mainPane.setCenter(welcomeLabel);
    }

    private void showMainPage() {
        Scene mainScene = new Scene(mainPane, 400, 300);
        primaryStage.setScene(mainScene);
        primaryStage.setTitle("Main Page");
    }

    private void showAlert(String message) {
        Alert alert = new Alert(Alert.AlertType.ERROR);
        alert.setTitle("Error");
        alert.setHeaderText(null);
        alert.setContentText(message);
        alert.showAndWait();
    }
}
