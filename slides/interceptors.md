#  Interceptors

```java

public class LoggingInterceptor implements HttpConnectionRequestInterceptor,
    HttpConnectionResponseInterceptor {

    Logger logger = Logger.getLogger(LoggingInterceptor.class.getCanonicalName());

    @Override
    public HttpConnectionInterceptorContext interceptRequest(
        HttpConnectionInterceptorContext context) {

        HttpURLConnection connection = context.connection.getConnection();
        logger.info("Making request to "+connection.getURL();
        return context;

    }

    @Override
    public HttpConnectionInterceptorContext interceptResponse(
        HttpConnectionInterceptorContext context) {

        HttpURLConnection connection = context.connection.getConnection();

        String msg = "Request Complete: "+ connection.getURL()
        + "/" + connection.getResponseCode();

        logger.info(msg);
        return context;
}
```
