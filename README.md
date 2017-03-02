# Hello-World
Hello everyone this is gaurav from Nagpue for the assessment of the human life

Please have a tea and coffee on time

basic needs to be fulfilled on time any how

#
package Test;

import java.net.MalformedURLException;

import org.openqa.selenium.By;
import org.openqa.selenium.remote.DesiredCapabilities;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;
import java.net.URL;
import io.appium.java_client.ios.IOSDriver;


public class Integrationapp {
  //Create instance for Appium Driver
	IOSDriver driver;
	
	@BeforeTest
  public void f() throws MalformedURLException{
				DesiredCapabilities caps = new DesiredCapabilities();
		caps.setCapability("platformName", "iOS");
		caps.setCapability("platformVersion", "10.2.1"); 
		caps.setCapability("deviceName", "version 6"); 
		caps.setCapability("UDID", "");
		caps.setCapability("app", "/Users/prakash/Library/Developer/Xcode/DerivedData/WebDriverAgent-brdadhpuduowllgivnnvuygpwhzy/Build/Products/Debug-iphoneos"); //Replace this with app path in your system
		 driver =new IOSDriver(new URL("http://127.0.0.1:4723/wb/hub"),caps);	}
	  
	@Test
	public void testiOS() throws InterruptedException {
		driver.findElement(By.name("Alerts")).click();
		driver.findElement(By.name("create App Alert")).click();
	}

}
#
