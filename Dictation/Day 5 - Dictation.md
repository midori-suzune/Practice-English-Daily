Technically, applying security with Spring Security in Spring application is simple
You have already implemented Spring application, so you know that the framework's philosophy starts with the management of the Spring context. You defined beans in the Spring context to allow the framework to manage these based on the configuration you specify

You use annotations to tell Spring what to do , expose endpoint , wrap method in transaction , intercept methods in aspects, and so on. The same is true with Spring Security configurations, which is where Spring Security comes into play. What you want is to use annotation , beans , and in general , spring fashioned configuration style comfortably when defining your application-level security. In a spring application, the behavior that you need to protect is defined by methods

To think about application-level security, you can consider your home and the way you allow access to it. Do you place the key under the entrance rug? Do you even have a key for  your front door? The same concept applies to application, and Spring Security helps you develop this functionality. It's a puzzle that offers plenty of choices for building the exact image that describes your system. You can choose to leave your house completely unsecured , or you can decide not to allow everyone to enter your home 

They way you configure security can be straightforward like hiding your key under the rug, or it can be more complicated like choosing a variety of alarm system , video cameras and locks. In your applications,  you have the same options , but as in real life , the more complexity you add , the more expensive it gets . In application , this cost refers to the way security affects maintainability and performance. 

