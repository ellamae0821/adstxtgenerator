<!DOCTYPE html>
<html>
<head>
    <title>Ads.txt</title>
</head>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
<body>



<div class="container">
    <div class="row">
        <div class="col-sm-12">
        	<h1 class="display-3">Ads.txt Generator</h1>
        </div>
    </div>
    <div class="row">
        <div class="col-sm-5">
            <label><input type="checkbox" name="WideOrbit" id="wideorbit" >WideOrbit</label> <br>
            <label><input type="checkbox" name="Rubicon" id="rubicon">Rubicon</label><br>
            <label><input type="checkbox" name="Targetspot" id="targetspot">Targetspot</label><br>
            <label><input type="checkbox" name="Adobe" id="adobe">Adobe</label><br>
            <label><input type="checkbox" name="Audio.ad" id="audio">Audio.ad</label><br>
            <label><input type="checkbox" name="Adswizz" id="adswizz">Adswizz</label> <br> <br>
            <input class="btn btn-primary" type="submit" id="submit" onclick="addLines()">
            <input class="btn btn-primary" type="submit" id="restart" value="Clear" onclick="clearChecked()">
        </div>
        <div class="col-sm-7">
            <div class="input-group">
                <div class="input-group-prepend">
                    <span class="input-group-text">Ads.txt</span>
                </div>
                <textarea class="form-control" aria-label="With textarea" id="output" rows="15"></textarea>
            </div>
        </div>
    </div>
</div>



<script type="text/javascript">

    var wideorbitVal =  ["wideorbit.com, <wopdpubid>, DIRECT, 009ac71611fe32ff"];
    var rubiconVal =    ["rubiconproject.com, 21134, RESELLER, 0bfd66d529a55807"];
    var tagetspotVal =  [
                            "targetspot.com, 29, RESELLER, feb28ed826dcf532",
                            "rubiconproject.com, 16418, RESELLER, 0bfd66d529a55807",
                            "rubiconproject.com, 9753, RESELLER, 0bfd66d529a55807",
                            "rubiconproject.com, 9755, RESELLER, 0bfd66d529a55807",
                            "spotxchange.com, 211833, RESELLER, 7842df1d2fe2db34",
                            "spotx.tv, 211833, RESELLER, 7842df1d2fe2db34",
                            "appnexus.com, 1577, RESELLER, f5ab79cb980f11d1",
                            "appnexus.com, 7265, RESELLER, f5ab79cb980f11d1",
                            "tritondigital.com, 44733, RESELLER, 19b4454d0b87b58b ",
                            "adswizz.com, targetspot, RESELLER"
                        ];
    var adobeVal =      [" "];
    var audioadVal =    [
                            "audio.ad, 30305, RESELLER",
                            "tritondigital.com, 28563, RESELLER, 19b4454d0b87b58b"
                        ];
    var adswizzVal =    [
                            "adswizz.com, kjlh, RESELLER",
                            "adswizz.com, wgnradio, RESELLER",
                            "adswizz.com, federatedmedia, RESELLER",
                            "adswizz.com, sinclair, RESELLER",
                            "adswizz.com, eldorado, RESELLER",
                            "adswizz.com, redapplemedia, RESELLER"
                        ];

    // window.onload = function () {

    // } 
    document.getElementById('wideorbit').value = wideorbitVal.join("\r\n");
    document.getElementById('rubicon').value = rubiconVal.join("\r\n");
    document.getElementById('targetspot').value = tagetspotVal.join("\r\n");
    document.getElementById('adobe').value = adobeVal.join("\r\n");
    document.getElementById('audio').value = audioadVal.join("\r\n");
    document.getElementById('adswizz').value = adswizzVal.join("\r\n");




    function addLines (){
        var selectedAds = [];
        var checkboxes = document.querySelectorAll('input[type=checkbox]:checked');

        for (var i=0; i<checkboxes.length; i++){

            selectedAds.push(checkboxes[i].value)
            // console.log(selectedAds);
            // console.log(selectedAds.push(checkboxes[i].value))
            
        }
        var stringAds = selectedAds.join("\r\n");
        document.getElementById("output").innerHTML = stringAds;
        // return selectedAds;
    }


    function clearChecked() {
       location.reload()
     
    }

//md


</script>
</script>
</body>
</html>

