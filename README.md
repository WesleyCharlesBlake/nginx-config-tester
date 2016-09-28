Update the `site.conf` located in [here](https://github.com/WesleyCharlesBlake/nginx-config-tester/blob/master/root/etc/nginx/conf.d/site.conf)

Save your changes.

Then run `docker-compose up`

If nginx has an issue with your conf, it shouldnt start, fix the directive thats broken and repeat.

Once your container is up, you can you attach it:

```
docker exec -i -t <CONTAINERID> sh
```

Then tail `/var/log/nginx/error.log` or `/var/log/nginx/access.log`

Hope this helpshttps://github.com/WesleyCharlesBlake/nginx-config-tester/blob/master/root/etc/nginx/conf.d/site.co your changesn