# Selenium
package demo;

import java.util.List;
import java.util.Set;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class XpUrbanLadder
{

	public static void main(String[] args) throws InterruptedException 
	{
		// TODO Auto-generated method stub
		System.setProperty("webdriver.chrome.driver","./software/chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.urbanladder.com/");
		Thread.sleep(5000);
		driver.findElement(By.xpath("//a[@data-gaaction='popup.auth.close']")).click();
		driver.findElement(By.xpath("//a[@class='featuredLinksBar__link' and @href='../../furniture-stores?src=header']")).click();
		List<WebElement> loc = driver.findElements(By.xpath("//h3[@class='_3JJeW']"));
		
		for(WebElement address:loc)
		{
			
			System.out.println(address.getText());
			
		}
		
	}
	

}
