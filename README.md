# Tugas-JS-DOM

SECTION 2-4

in HTML
```
...
<h1 id="judul">Ini adalah judul</h1>
	<p id="teks">Ini adalah teks</p>
	<button onclick="ubahWarnaBackground()">Ubah Warna Background</button>
	<button onclick="ubahUkuranFont()">Ubah Ukuran Font</button>
	<button onclick="ubahTeks()">Ubah Teks</button>
...
```

in JS
```
...
function ubahWarnaBackground() {
			document.getElementById("judul").style.backgroundColor = "#007bff";
			document.getElementById("teks").style.backgroundColor = "#007bff";
			document.body.style.backgroundColor = "#f8f9fa";
		}

		function ubahUkuranFont() {
			document.getElementById("judul").style.fontSize = "30px";
			document.getElementById("teks").style.fontSize = "16px";
			document.body.style.fontSize = "18px";
		}

		function ubahTeks() {
			document.getElementById("judul").innerHTML = "Ini adalah judul yang baru";
			document.getElementById("teks").innerHTML = "Ini adalah teks yang baru";
		}
...
```
