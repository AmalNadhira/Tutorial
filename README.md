# WELCOME PART.



package Minesweeper;


import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.HBox;
import javafx.scene.layout.Pane;
import javafx.scene.paint.Color;
import javafx.scene.text.Font;
import javafx.scene.text.FontPosture;
import javafx.scene.text.FontWeight;
import javafx.scene.text.Text;
import javafx.stage.Stage;

public class Welcome extends Application{
	 @Override
	 public void start(Stage primaryStage){		
		 Pane pane = new Pane();
		 pane.setPadding(new Insets(100, 100, 100, 100));
		    Text text1 = new Text(600, 40, "     M I N E S W E E P E R  G A M E S  ");
		    Text text2 = new Text(530,60, "           Y O U R  G A M I N G  W O R L D ");
		    text1.setFont(Font.font("Platino", FontWeight.BOLD, 
		      FontPosture.ITALIC, 15));
		    text1.setFill(Color.BLACK);
		    text2.setFont(Font.font("Comic Sans MS", FontWeight.BOLD, 
				      FontPosture.REGULAR, 15));
				    text2.setFill(Color.BROWN);
				    
						 HBox hBox = new HBox();
						 hBox.setPadding(new Insets(580, 580, 540, 470));
						    hBox.setSpacing(10);
						    hBox.setAlignment(Pos.BOTTOM_CENTER);
						    ImageView imageAbout = new ImageView(new Image("http://icons.iconarchive.com/icons/zhoolego/material/24/Games-icon.png"));
						    Button btAbout = new Button(" H O W T O P L A Y ? ");
						    btAbout.setGraphic(imageAbout);
						    
						    
						    ImageView imageGame = new ImageView(new Image("http://icons.iconarchive.com/icons/hopstarter/soft-scraps/24/Games-icon.png"));
						    Button btGame = new Button("G A M E");
						    btGame.setGraphic(imageGame);
						    
						 
						    
						    ImageView imageSuggest = new ImageView(new Image("http://icons.iconarchive.com/icons/ccard3dev/dynamic-yosemite/24/Utilities-Feedback-Assistant-icon.png"));
						    Button btfb = new Button("S U G G E S T I O N");
						    btfb.setGraphic(imageSuggest);
						    
						    

						    
						    hBox.getChildren().addAll(btAbout, btGame,  btfb);
		    
		    pane.getChildren().add(getHBox()); 
		    pane.getChildren().add(text1); 
		    pane.getChildren().add(text2); 
		    pane.getChildren().add (hBox); 
		    
		    
		    
		    
		    btAbout.setOnAction(new EventHandler<ActionEvent>() {
		        @Override public void handle(ActionEvent e) {
		            AboutUs about= new AboutUs();
		            about.start(primaryStage);
		            
		        }
		    });
		    
		    btfb.setOnAction(new EventHandler<ActionEvent>() {
		        @Override public void handle(ActionEvent e) {
		            Feedback fb= new Feedback();
		            fb.start(primaryStage);
		            
		        }
		    });
		    
		    btGame.setOnAction(new EventHandler<ActionEvent>() {
		        @Override public void handle(ActionEvent e) {
		           Game Game= new Game();
		           Game.start(primaryStage);		            
		        }
		    });
		    
		    

		    Scene scene = new Scene(pane);
		    primaryStage.setTitle("Hello, Welcome!"); // Set the stage title
		    primaryStage.setScene(scene); // Place the scene in the stage
		    primaryStage.show();
		    primaryStage.centerOnScreen();// Display the stage
		 
	 }
	 public static void main(String[] args) {
		    launch(args);
		  }
	 
	 protected void ReceiptCalculator() {
		// TODO Auto-generated method stub
		
	}

	public HBox getHBox() {
		    HBox hBox = new HBox(95); 
		    hBox.setPadding(new Insets(100, 800, 200, 300));
		  
		    ImageView imageView = new ImageView(new Image("http://i.imgur.com/X02uxgK.png"));
		    hBox.getChildren().add(imageView);
		    return hBox;
		  }}
