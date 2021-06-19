<!DOCTYPE html>
<html>

<head>
    <title>MySejahtera Hotspot</title>

    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
        integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
        crossorigin="" />

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"
        integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
        integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
        crossorigin=""></script>

    <style>
        html,
        body {
            height: 100%;
            margin: 0;
        }

        #map {
            width: 100%;
            height: 95%;
        }
    </style>
</head>

<body>
    <form>
        <label>Select your state:</label>
        <select id="states" name="state">
            <option value="1">Johor</option>
            <option value="2">Kedah</option>
            <option value="3">Kelantan</option>
            <option value="4">Melaka</option>
            <option value="5">Negeri Sembilan</option>
            <option value="6">Pahang</option>
            <option value="7">Penang</option>
            <option value="8">Perak</option>
            <option value="9">Perlis</option>
            <option value="12">Sabah</option>
            <option value="13">Sarawak</option>
            <option value="10">Selangor</option>
            <option value="11">Terengganu</option>
            <option value="14" selected>Federal Territory of Kuala Lumpur</option>
            <option value="15">Federal Territory of Labuan</option>
            <option value="16">Federal Territory of Putrajaya</option>
        </select>
    </form>

    <div id="map"></div>

    <script>
        var state = $('#states').val();
        getMap(state);

        $('#states').on('change', function () {
            state = $('#states').val();
            getMap(state);
        });

        $.ajax({
            url: 'last-update.json',
            dataType: 'json',
            timeout: 5000,
            success: function (data) {
                $("#last-update").text(data['last-update'])
            },
            error: function () {
                $("#last-update").text('2021-06-15')
            }
        });

        function getMap(state) {
            var zoom = {
                '1': 9,
                '2': 9,
                '3': 9,
                '4': 10.5,
                '5': 9.5,
                '6': 9,
                '7': 10.5,
                '8': 9.5,
                '9': 11,
                '10': 10,
                '11': 8.5,
                '12': 8,
                '13': 7,
                '14': 11.5,
                '15': 12,
                '16': 13,
            }

            var center = {
                '1': [1.891816231746032, 103.49781690793652],
                '2': [5.861430566265059, 100.67029332530122],
                '3': [5.199608448780487, 102.06351577073173],
                '4': [2.290535240310077, 102.30847203100777],
                '5': [2.618115251655629, 102.08174941721853],
                '6': [4.071478952606635, 102.32340633175355],
                '7': [5.326611172413791, 100.41983951724136],
                '8': [4.733874, 101.14707000581394],
                '9': [6.524751999999999, 100.22751252631578],
                '10': [3.355404307017544, 101.50504664035088],
                '11': [4.825278525714285, 102.89730278285715],
                '12': [5.27816915, 116.97592164999999],
                '13': [2.738490452054794, 113.39022178082192],
                '14': [3.1392120930232563, 101.69246448837208],
                '15': [5.314517, 115.221615],
                '16': [2.933356648648649, 101.68667875675675],
            }

            var data = {
                '1': 'data/Johor-points.json-points-cases.json',
                '2': 'data/Kedah-points.json-points-cases.json',
                '3': 'data/Kelantan-points.json-points-cases.json',
                '4': 'data/Melaka-points.json-points-cases.json',
                '5': 'data/Negeri%20Sembilan-points.json-points-cases.json',
                '6': 'data/Pahang-points.json-points-cases.json',
                '7': 'data/Penang-points.json-points-cases.json',
                '8': 'data/Perak-points.json-points-cases.json',
                '9': 'data/Perlis-points.json-points-cases.json',
                '10': 'data/selangor-points.json-points-cases.json',
                '11': 'data/Terengganu-points.json-points-cases.json',
                '12': 'data/Sabah-points.json-points-cases.json',
                '13': 'data/Sarawak-points.json-points-cases.json',
                '14': 'data/Federal%20Territory%20of%20Kuala%20Lumpur-points.json-points-cases.json',
                '15': 'data/Labuan-points.json-points-cases.json',
                '16': 'data/Federal%20Territory%20of%20Putrajaya-points.json-points-cases.json',
            }

            var container = L.DomUtil.get('map');
            if (container != null) {
                container._leaflet_id = null;
            }

            var map = L.map('map').fitWorld();
                L.tileLayer('https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token=pk.eyJ1IjoiemFoaXJ5dXNvZjkyIiwiYSI6ImNqNHBiM3AxbTF2b20zM3Fzb2NlZWRicHIifQ.vdr1R7iMa5V8D6nNXKf2xw', {
                    attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors, ' + 'Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
                    id: 'mapbox/streets-v11',
                    tileSize: 512,
                    zoomOffset: -1
                }).addTo(map);

                function onLocationFound(e) {
                    var radius = e.accuracy / 2;

                    L.marker(e.latlng).addTo(map).bindPopup("You are within " + radius + " meters from this point").openPopup();
                    L.circle(e.latlng, radius).addTo(map);
                }

                function onLocationError(e) {
                    alert(e.message);
                }

                map.on('locationfound', onLocationFound);
                map.on('locationerror', onLocationError);

                map.locate({ setView: true, maxZoom: 16 });

            $.ajax({
                url: 'data/malaysia.geojson',
                dataType: 'json',
                timeout: 5000,
                success: function (data) {
                    if (data.features) {
                        L.geoJSON(data.features).addTo(map);
                    }
                }
            });

            $.ajax({
                url: data[state],
                dataType: 'json',
                timeout: 5000,
                success: function (data) {
                    for (var i = 0; i < data.length; i++) {
                        if (data[i][2] > 0) {
                            const circle = L.circle([data[i][0], data[i][1]], {
                                color: 'red',
                                fillColor: '#f03',
                                fillOpacity: 0.5,
                                radius: data[i][2],
                            }).addTo(map);
                        }
                    }
                }
            });
        }
    </script>
</body>

</html>