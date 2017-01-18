# PeopleAPI_Microservice
A sample microservice written using Spring Boot

A guide for getting started with Spring Boot microservices can be found in http://tharindue.blogspot.com/2017/01/a-quick-start-guide-for-writing.html

Instructions for Running the Sample
-----------------------------------

1. Build the project using Maven. If not you can simply use the jar file in target directory here.
2. Run the jar file using the command "java -jar people.api-1.0.jar --server.port=8081" . You can use any port number.
3. The microservice will be started in the given port.
4. Send a HTTP GET request to http://hostname:port/people/skills . 

If you are using curl, simply use the command "curl -X http://hostname:port/people/skills

You should see the output. Here the service accepts a JSON Web Token (JWT) in the HTTP Header "X-JWT-Assertion". In the JWT, the username should be included in the claim "http://wso2.org/claims/enduser".  

You can send the following sample request for testing. Make sure to put your hostname and port number in the URL at the end.

curl -X GET --header "X-JWT-Assertion: eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6ImFfamhOdXMyMUtWdW9GeDY1TG1rVzJPX2wxMCJ9.eyJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC9hcHBsaWNhdGlvbnRpZXIiOiJVbmxpbWl0ZWQiLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC9rZXl0eXBlIjoiUFJPRFVDVElPTiIsImh0dHA6XC9cL3dzbzIub3JnXC9jbGFpbXNcL3ZlcnNpb24iOiJ2MS4wLjAiLCJpc3MiOiJ3c28yLm9yZ1wvcHJvZHVjdHNcL2FtIiwiaHR0cDpcL1wvd3NvMi5vcmdcL2NsYWltc1wvYXBwbGljYXRpb25uYW1lIjoibXlwZW9wbGVhcHAiLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC9lbmR1c2VyIjoiYWRtaW5AY2FyYm9uLnN1cGVyIiwiaHR0cDpcL1wvd3NvMi5vcmdcL2NsYWltc1wvZW5kdXNlclRlbmFudElkIjoiLTEyMzQiLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC9zdWJzY3JpYmVyIjoiYWRtaW4iLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC90aWVyIjoiVW5saW1pdGVkIiwiaHR0cDpcL1wvd3NvMi5vcmdcL2NsYWltc1wvYXBwbGljYXRpb25pZCI6IjUiLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC91c2VydHlwZSI6IkFQUExJQ0FUSU9OIiwiZXhwIjoxNDg0Njk1NDAzLCJodHRwOlwvXC93c28yLm9yZ1wvY2xhaW1zXC9hcGljb250ZXh0IjoiXC9wZW9wbGVhcGlcL3YxLjAuMCJ9.PwM17M5G2vGsInG5bmCSQBnfY5t6eQyR1vwrzsfM4SWZft4wh/u9xJfayPpjvkW/yj4bD/C7mxTZllfle0ppm0dYWMh1i1W/FZhHd9QGGXHq3zGpv9WOLbt6hCnCrjTE93ex48WcYi1ejjMa9NpDFyaW8UFQBbLkMB+Sj2tNpOY=" http://hostname:port/people/skills 
