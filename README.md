# CashHero_Mobile
web mobile
## 部署
```text
docker build ./docker/Dockerfile -t cashhero-mobile .
docker compose up -d
docker compose down -v
```
```text
占用IP:
172.88.0.104

cloudflare tunnel分配:
chweb.freefree.vip -> 172.88.0.104:80
```
```text
cloudflare cache rules:
(http.host eq "chweb.freefree.vip" and http.request.uri.path.extension eq "mp3") or (http.host eq "chweb.freefree.vip" and http.request.uri.path.extension eq "png") or (http.host eq "chweb.freefree.vip" and http.request.uri.path.extension eq "js") or (http.host eq "chweb.freefree.vip" and http.request.uri.path.extension eq "json") or (http.host eq "chweb.freefree.vip" and http.request.uri.path.extension eq "jpg")
```
