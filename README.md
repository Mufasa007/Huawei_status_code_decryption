<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>华为招聘状态在线解密</title>
</head>
<body>
    <textarea type="text" id="txt" rows="10" cols="50"></textarea>
    <br>
    <button id="btn">点击解密</button>
    <h2>解密结果：</h2>
    <p id="result"></p>
    <script src="./jsencrypt.min.js"></script>
    <script>
        var txt = document.getElementById('txt');
        var btn = document.getElementById('btn');
        var result = document.getElementById('result');
        var a = new JSEncrypt();
        a.setPrivateKey("MIICdgIBADANBgkqhkiG9w0BAQEFAASCAmAwggJcAgEAAoGBAK0UVX5n7zgk7KXtBT4oCgTo/rMwzxnhNi1/I0gakyUtF28WHOYPUCespbF1IUong67usS43d0FlBCM8pe/gaZI0LNvIj+29gDfZpXGhtrjVrN+aP8gx0NHZI9kHaf38bbqqO+r7dXPckKY8twfVPYZIsdoL0gvxYIPTVm+A/QMfAgMBAAECgYA4shx/V9SI86+Beu7ouXzuttQYJrjwpVF1/du01t+0ody3SusUgZekJ23vf4r0G5WLTC1GEm1CQrDkSg2hUkXCT+pUETZEKD0svnFHG4JTpeLcxV/igbqGICrf+NhBwzb7JltraY92x5Ku+OBh606OPMAax+9S78mFh/t5yqGuYQJBAO0e4xLs1aclhn7++iK9R3gEHZMI3ZkOYABiReeSWZqygujlJNMpw9s/Oolibubm9411aV3N8LFDo8FiqkCwOKMCQQC63CBaUEXAxD0dz1+7iO5h06e+RmuB8nqvxVdcas9RK8JN+O3g/8tlU0AoGuVlY4+ZJrHubqGtMdjZgy4Rd0dVAkATsnEibVICJHfbrMqSgC6jpZPfVukxgaQv4/nylpGi7Bk7x20brWh7mfD+4JJd0+nUcmBiTm0kDH5Z3hxOa1UJAkEAsPabpSx0gtTWVI76SO6rY/ZA3FBwrEZprmEkFSAKawMYJyPilL1rcPBgyBqAuX6Kli4xQG+BqjaU+ZnkXSIraQJAaZKaXjoq4Ip7zGvHzLySNDAtdZyi868xakSf/B8C9fvDqboS48oRWTdV9RJmsWwd1oaPPo0E8DhO5Ix1kbEMew==")
        btn.onclick = function() {
            try{
                result.innerText = decodeURIComponent(a.decryptLong2(txt.value));
            } catch(e) {
                alert('出错啦，请检查你输入的密文是否正确');
            }
        }
    </script>
</body>
</html>
