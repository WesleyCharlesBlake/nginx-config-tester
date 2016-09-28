This docker images was specifically created to help test nginx and rewrite directives. We often create 1000s of lines of rewrites, and sometimes human error does creep in.

This allowed us to test the 301 directives before having to deploy using our config management tools. It could easily be hacked to suit your use case.

Update the `site.conf` located in [here](https://github.com/WesleyCharlesBlake/nginx-config-tester/blob/master/root/etc/nginx/conf.d/site.conf)

Save your changes.

Then run `docker-compose up`

If nginx has an issue with your conf, it shouldnt start, fix the directive thats broken and repeat.

Once your container is up, you can you attach it:

```
docker exec -i -t <CONTAINERID> sh
```

Then tail `/var/log/nginx/error.log` or `/var/log/nginx/access.log`

Hope this helps!

