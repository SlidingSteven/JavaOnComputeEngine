# JavaOnComputeEngine

The master branch is for the Django app and the Java Branch is for... the java program.

This is basically the Java code for random number generator- import java.io.IOException; import java.io.PrintWriter; import java.util.Random; and then within the servlet we need to place Random rand = new Random(); int num = rand.nextInt(1000000); num += 1;

This video will get you started with Tomcat on ComputeEngine- https://youtu.be/CXHnfscyIsU once you have the generic page working you can modify their hello world example and just drop those lines in the code like this.

The simplest possible servlet.

    import java.io.IOException; 
    import java.io.PrintWriter;
    import java.util.ResourceBundle; 
    import java.io.IOException; 
    import java.io.PrintWriter; 
    import java.util.Random; 
    import javax.servlet.ServletException; 
    import javax.servlet.http.HttpServlet; 
    import javax.servlet.http.HttpServletRequest; 
    import javax.servlet.http.HttpServletResponse; 

    //@author James Duncan Davidson 
    public class HelloWorldExample extends HttpServlet { 
     private static final long serialVersionUID = 1L; 
     @Override public void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException, ServletException { 
      ResourceBundle rb = ResourceBundle.getBundle("LocalStrings",request.getLocale());
      response.setContentType("text/html");
      PrintWriter out = response.getWriter(); 
      out.println(""); 
      out.println(""); 
      out.println("<meta charset="UTF-8" />"); 
      String title = rb.getString("helloworld.title"); 
      out.println("<body bgcolor="white">");
      //INSERT CODE HERE
      PrintWriter printWriter  = response.getWriter();
      Random rand  = new Random();
      int num = rand.nextInt(1000000);
      num += 1;
      out.println( num );
      //END OF OUR CODE
      out.println("</body>");
      out.println("</html>");
    } }
