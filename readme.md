# Filebrowser API

## Login

```bash
curl 'http://localhost:8195/api/login' -X POST -H 'User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:136.0) Gecko/20100101 Firefox/136.0' -H 'Accept: */*' -H 'Accept-Language: en-US,en;q=0.5' -H 'Accept-Encoding: gzip, deflate, br, zstd' -H 'Referer: http://localhost:8195/login?redirect=/files/' -H 'Content-Type: application/json' -H 'Origin: http://localhost:8195' -H 'Connection: keep-alive' -H 'Sec-Fetch-Dest: empty' -H 'Sec-Fetch-Mode: cors' -H 'Sec-Fetch-Site: same-origin' -H 'Priority: u=0' --data-raw '{"username":"admin","password":"admin","recaptcha":""}'
```

```json

{
  "username": "admin",
  "password": "admin",
  "recaptcha": ""
}
```
> http://localhost:8195/api/login

> Response: **Cookie**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJsb2NhbGUiOiJlbiIsInZpZXdNb2RlIjoibW9zYWljIiwic2luZ2xlQ2xpY2siOmZhbHNlLCJwZXJtIjp7ImFkbWluIjp0cnVlLCJleGVjdXRlIjp0cnVlLCJjcmVhdGUiOnRydWUsInJlbmFtZSI6dHJ1ZSwibW9kaWZ5Ijp0cnVlLCJkZWxldGUiOnRydWUsInNoYXJlIjp0cnVlLCJkb3dubG9hZCI6dHJ1ZX0sImNvbW1hbmRzIjpbXSwibG9ja1Bhc3N3b3JkIjpmYWxzZSwiaGlkZURvdGZpbGVzIjp0cnVlLCJkYXRlRm9ybWF0Ijp0cnVlfSwiaXNzIjoiRmlsZSBCcm93c2VyIiwiZXhwIjoxNzQ1ODUzMTQ3LCJpYXQiOjE3NDU4NDU5NDd9.zsAYxWawX8y7Kr9d3ZN4LvJ8fp0eGwHyy8uipKyCGMs


## Get files/Folders

```bash
curl 'http://localhost:8195/api/resources/' -H 'User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:136.0) Gecko/20100101 Firefox/136.0' -H 'Accept: */*' -H 'Accept-Language: en-US,en;q=0.5' -H 'Accept-Encoding: gzip, deflate, br, zstd' -H 'Referer: http://localhost:8195/files/' -H 'X-Auth: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJsb2NhbGUiOiJlbiIsInZpZXdNb2RlIjoibW9zYWljIiwic2luZ2xlQ2xpY2siOmZhbHNlLCJwZXJtIjp7ImFkbWluIjp0cnVlLCJleGVjdXRlIjp0cnVlLCJjcmVhdGUiOnRydWUsInJlbmFtZSI6dHJ1ZSwibW9kaWZ5Ijp0cnVlLCJkZWxldGUiOnRydWUsInNoYXJlIjp0cnVlLCJkb3dubG9hZCI6dHJ1ZX0sImNvbW1hbmRzIjpbXSwibG9ja1Bhc3N3b3JkIjpmYWxzZSwiaGlkZURvdGZpbGVzIjp0cnVlLCJkYXRlRm9ybWF0Ijp0cnVlfSwiaXNzIjoiRmlsZSBCcm93c2VyIiwiZXhwIjoxNzQ1ODUzMTQ3LCJpYXQiOjE3NDU4NDU5NDd9.zsAYxWawX8y7Kr9d3ZN4LvJ8fp0eGwHyy8uipKyCGMs' -H 'Connection: keep-alive' -H 'Cookie: auth=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJsb2NhbGUiOiJlbiIsInZpZXdNb2RlIjoibW9zYWljIiwic2luZ2xlQ2xpY2siOmZhbHNlLCJwZXJtIjp7ImFkbWluIjp0cnVlLCJleGVjdXRlIjp0cnVlLCJjcmVhdGUiOnRydWUsInJlbmFtZSI6dHJ1ZSwibW9kaWZ5Ijp0cnVlLCJkZWxldGUiOnRydWUsInNoYXJlIjp0cnVlLCJkb3dubG9hZCI6dHJ1ZX0sImNvbW1hbmRzIjpbXSwibG9ja1Bhc3N3b3JkIjpmYWxzZSwiaGlkZURvdGZpbGVzIjp0cnVlLCJkYXRlRm9ybWF0Ijp0cnVlfSwiaXNzIjoiRmlsZSBCcm93c2VyIiwiZXhwIjoxNzQ1ODUzMTQ3LCJpYXQiOjE3NDU4NDU5NDd9.zsAYxWawX8y7Kr9d3ZN4LvJ8fp0eGwHyy8uipKyCGMs' -H 'Sec-Fetch-Dest: empty' -H 'Sec-Fetch-Mode: cors' -H 'Sec-Fetch-Site: same-origin' -H 'Priority: u=4'
```

> http://localhost:8195/api/resources/Pictures/Wallpapers/

> Response: 
```json
{
  "items":[
      {"path":"/Desktop","name":"Desktop","size":4096,"extension":"","modified":"2025-04-21T15:48:46.939388249Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/development","name":"development","size":4096,"extension":"","modified":"2025-04-24T17:11:48.071611979Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/docker","name":"docker","size":4096,"extension":"","modified":"2025-04-25T14:53:15.574459032Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Documents","name":"Documents","size":4096,"extension":"","modified":"2025-04-22T18:09:56.33188268Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Downloads","name":"Downloads","size":12288,"extension":"","modified":"2025-04-25T15:49:52.704890108Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/filebrowser","name":"filebrowser","size":4096,"extension":"","modified":"2025-04-23T19:26:48.862051383Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/go","name":"go","size":4096,"extension":"","modified":"2025-04-21T18:09:06.973623913Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Music","name":"Music","size":4096,"extension":"","modified":"2025-03-07T22:08:22.359337008Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Pictures","name":"Pictures","size":4096,"extension":"","modified":"2024-08-26T18:28:46.218657595Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Postman","name":"Postman","size":4096,"extension":"","modified":"2024-01-16T14:13:46.391356649Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Public","name":"Public","size":4096,"extension":"","modified":"2023-11-02T11:38:49.03249215Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/snap","name":"snap","size":4096,"extension":"","modified":"2025-04-02T20:05:07.37725738Z","mode":2147484096,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Soporte","name":"Soporte","size":4096,"extension":"","modified":"2024-08-14T19:03:32.159748035Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Templates","name":"Templates","size":4096,"extension":"","modified":"2023-11-02T11:38:49.03249215Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/Videos","name":"Videos","size":4096,"extension":"","modified":"2025-04-22T19:27:52.621678785Z","mode":2147484141,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/workstation","name":"workstation","size":4096,"extension":"","modified":"2025-04-21T18:00:15.421088495Z","mode":2147484157,"isDir":true,"isSymlink":false,"type":""},
      {"path":"/casas.mp4","name":"casas.mp4","size":61439000,"extension":".mp4","modified":"2024-01-16T15:28:53.722779316Z","mode":420,"isDir":false,"isSymlink":false,"type":"video"}
  ],
  "numDirs":16,
  "numFiles":1,
  "sorting":{"by":"name","asc":false},
  "path":"/",
  "name":"srv",
  "size":4096,
  "extension":"",
  "modified":"2025-04-28T13:08:25.23153516Z",
  "mode":2147484136,
  "isDir":true,
  "isSymlink":false,
  "type":""
}
```

## Get image
```bash
curl 'http://localhost:8195/api/preview/big/Pictures/Wallpapers/test.png?auth=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJsb2NhbGUiOiJlbiIsInZpZXdNb2RlIjoibW9zYWljIiwic2luZ2xlQ2xpY2siOmZhbHNlLCJwZXJtIjp7ImFkbWluIjp0cnVlLCJleGVjdXRlIjp0cnVlLCJjcmVhdGUiOnRydWUsInJlbmFtZSI6dHJ1ZSwibW9kaWZ5Ijp0cnVlLCJkZWxldGUiOnRydWUsInNoYXJlIjp0cnVlLCJkb3dubG9hZCI6dHJ1ZX0sImNvbW1hbmRzIjpbXSwibG9ja1Bhc3N3b3JkIjpmYWxzZSwiaGlkZURvdGZpbGVzIjp0cnVlLCJkYXRlRm9ybWF0Ijp0cnVlfSwiaXNzIjoiRmlsZSBCcm93c2VyIiwiZXhwIjoxNzQ1ODUzMTQ3LCJpYXQiOjE3NDU4NDU5NDd9.zsAYxWawX8y7Kr9d3ZN4LvJ8fp0eGwHyy8uipKyCGMs&inline=true&key=1699885607511' -H 'User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:136.0) Gecko/20100101 Firefox/136.0' -H 'Accept: image/avif,image/webp,image/png,image/svg+xml,image/*;q=0.8,*/*;q=0.5' -H 'Accept-Language: en-US,en;q=0.5' -H 'Accept-Encoding: gzip, deflate, br, zstd' -H 'Connection: keep-alive' -H 'Referer: http://localhost:8195/files/Pictures/Wallpapers/test.png' -H 'Cookie: auth=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJsb2NhbGUiOiJlbiIsInZpZXdNb2RlIjoibW9zYWljIiwic2luZ2xlQ2xpY2siOmZhbHNlLCJwZXJtIjp7ImFkbWluIjp0cnVlLCJleGVjdXRlIjp0cnVlLCJjcmVhdGUiOnRydWUsInJlbmFtZSI6dHJ1ZSwibW9kaWZ5Ijp0cnVlLCJkZWxldGUiOnRydWUsInNoYXJlIjp0cnVlLCJkb3dubG9hZCI6dHJ1ZX0sImNvbW1hbmRzIjpbXSwibG9ja1Bhc3N3b3JkIjpmYWxzZSwiaGlkZURvdGZpbGVzIjp0cnVlLCJkYXRlRm9ybWF0Ijp0cnVlfSwiaXNzIjoiRmlsZSBCcm93c2VyIiwiZXhwIjoxNzQ1ODUzMTQ3LCJpYXQiOjE3NDU4NDU5NDd9.zsAYxWawX8y7Kr9d3ZN4LvJ8fp0eGwHyy8uipKyCGMs' -H 'Sec-Fetch-Dest: image' -H 'Sec-Fetch-Mode: no-cors' -H 'Sec-Fetch-Site: same-origin' -H 'Priority: u=5, i' -H 'Pragma: no-cache' -H 'Cache-Control: no-cache'
```

> http://localhost:8195/api/preview/big/Pictures/Wallpapers/test.png?auth=cookie
