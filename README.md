Update the `site.conf` located in (https://github.com/WesleyCharlesBlake)[here].

Save,

then run `docker-compose up`

If nginx has an issue with your conf, it shouldnt start, fix the directive thats broken and repeat.

Once your container is up, you can you attach it:

```
docker exec -i -t <CONTAINERID> sh
```

Then tail `/var/log/nginx/error.log` or `/var/log/nginx/access.log`

Hope this helps!