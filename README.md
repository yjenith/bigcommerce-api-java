Bigcommerce API V2 Java Client
==============================

Java client for accessing the Bigcommerce REST API.

Installation
------------

Import the .jar file into your classpath, or download and compile the source
package in ./src

Usage
-----

Using the store facade:

```
import com.bigcommerce.api.Store;

class BigcommerceApiTest
{

	public static void main(String[] args)
	{
		String storeUrl = "https://examplestore.com";
		String username = "admin";
		String apiKey   = "akjfalksjflksjflaskdjflasdk";

		Store api = new Store(storeUrl, username, apiKey);
		Collection<Order> orders = api.getOrders().listAll();

		for (Order order : orders) {
			System.out.println("Customer ID:" + order.getCustomerId());
			System.out.println("Order ID:" + order.getId());
			System.out.println("Order Status:" + order.getStatus());
		}
	}

}
```
See also: https://github.com/yjenith/bigcommerce-api-java-lite
