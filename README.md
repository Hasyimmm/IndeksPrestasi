<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>tugas pertemuan 18</title>
</head>
<body>
    <script>
        function hitung() {
            // get the input values
            var quis = parseInt(document.getElementById("quis").value);
            var tugas = parseInt(document.getElementById("tugas").value);
            var uts = parseInt(document.getElementById("uts").value);
            var uas = parseInt(document.getElementById("uas").value);
            // calculate the weighted score
            var total = (quis * 0.1) + (tugas * 0.2) + (uts * 0.3) + (uas * 0.4);
            // determine the index achievement
            var indeks = "";
            if (total >= 80) {
                indeks = "A";
            } else if (total >= 68) {
                indeks = "B";
            } else if (total >= 55) {
                indeks = "C";
            } else if (total >= 38) {
                indeks = "D";
            } else {
                indeks = "E";
            }
            // set the output values
            document.getElementById("indeks").value = indeks;
            // determine the achievement description
            var keterangan = "";
            switch (indeks) {
                case "A":
                    keterangan = "Lulus dengan Sangat Baik";
                    break;
                case "B":
                    keterangan = "Lulus dengan Baik";
                    break;
                case "C":
                    keterangan = "Lulus dengan Cukup";
                    break;
                case "D":
                    keterangan = "Lulus dengan Kurang";
                    break;
                case "E":
                    keterangan = "Tidak Lulus";
                    break;
            }
            document.getElementById("keterangan").value = keterangan;
        }
        function resetForm() {
            document.getElementById("quis").value = '';
            document.getElementById("tugas").value = '';
            document.getElementById("uts").value = '';
            document.getElementById("uas").value = '';
            document.getElementById("indeks").value = '';
            document.getElementById("keterangan").value = '';
        }
    </script>
    <style>
        table,
        th,
        td {
            border: 1px solid black;
            border-collapse: collapse;
        }
        th,
        td {
            padding: 5px;
            text-align: left;
        }
    </style>
    </head>
    <body>
        <table border="1" align="center" width="70%">
            <tr>
                <td width="100%" colspan="4">
                    <h2 align="center">MENGHITUNG INDEKS PRESTASI</h2>
                </td>
            </tr>
            <tr>
            <tr>
                <th>Quis (10%) :</th>
                <th>Tugas (20%) :</th>
                <th>UTS (30%) :</th>
                <th>UAS (40%) :</th>
            </tr>
            <tr>
                <td><input type="number" id="quis" value=""></td>
                <td><input type="number" id="tugas" value=""></td>
                <td><input type="number" id="uts" value=""></td>
                <td><input type="number" id="uas" value=""></td>
            </tr>
            <tr>
                <td width="100%" colspan="4">
                    <center>
                        <button onclick="hitung()">Hitung</button>
                        <button onclick="resetForm()">Ulang</button>
                    </center>
                </td>
            </tr>
            <tr>
              <td width="100%" colspan="4">
                    <center>
                        Indeks Prestasi :
                        <input type="text" id="indeks" readonly> Keterangan :
                        <input type="text" id="keterangan" readonly>
                    </center>
                </td>
            </tr>
        </table>
        </center>
    </body>

</html>
