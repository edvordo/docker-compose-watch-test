## From the repository as is

- `docker compose watch`
- `docker compose exec app bash`
    - `ls -al`
        - empty directory `/var/www/html`

## With `COPY . /var/www/html` in Dockerfile

- add `COPY . /var/www/html`
- `docker compose build app`
- `docker compose watch`
- change `index.html` to whatever
- changes are reflected in container and in the browser (http://localhost:8080/index.html)
- kill `watch`
- `docker compose down`
- `docker compose watch`
  - no changes made to `index.html` can be seen in container or in browser
