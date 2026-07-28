<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Base64 Viewer</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:#111;
    color:#fff;
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
}

.container{
    width:90%;
    max-width:800px;
    background:#1b1b1b;
    padding:30px;
    border-radius:12px;
    box-shadow:0 0 20px rgba(255,255,255,.08);
}

h1{
    text-align:center;
    margin-bottom:20px;
}

.code{
    background:#000;
    color:#00ff88;
    padding:15px;
    border-radius:8px;
    word-break:break-all;
    font-size:15px;
    line-height:1.6;
}
</style>
</head>
<body>

<div class="container">
    <h1>Base64 Code</h1>

    <div class="code">
RkxBRyhoYWxvIGd1YSBiaXNhIGhhY2sgd2liZXNpdGUgY3VtYW4gZGVuZ2FuIGFsZXJ0IGRvY3VtZW50IGNvb2tpZSk=
    </div>
</div>

</body>
</html>
