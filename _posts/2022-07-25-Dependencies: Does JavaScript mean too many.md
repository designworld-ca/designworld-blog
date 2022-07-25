## Dependencies: Does JavaScript mean too many?
[Insightful article by Charles Chen](https://chrlschn.medium.com/the-case-for-c-and-net-72ee933da304) on how your choice of programming language affects how many dependencies you will have to manage and secure. 

JavaScript is a necessity for web applications but if your programming language has a good library you won't need as much of it.

This chart from GitHub's State of the Octoverse shows when you use JavaScript you will have many, many more transitive dependencies
![Dependencies Graph](/images/Dependencies.png)

Why is this an issue?
- Increases your risk of vulnerabilities in dependencies
- Possible web performance issues: Slow page loads anyone?
- Containers look even more opaque as to what's inside them

Best quote of the article

> I just want a low-fuss, low-drama, low-maintenance, high-performance, highly secure programming language and runtime for my applications

Tags: [dependencies] [itsecurityoperations] [cybersecurity]
