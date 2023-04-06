# Tugas-JS-DOM

SECTION 2

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

SECTION 5

CONTOH 1

in HTML
```
...
<div id="container"></div>
...
```

in JS
```
...
// Membuat elemen HTML baru
		const p = document.createElement("p");

		// Menambahkan konten ke dalam elemen HTML baru
		p.innerHTML = "Ini adalah contoh program createElement() dalam satu use case.";

		// Menambahkan elemen HTML baru ke dalam container
		const container = document.getElementById("container");
		container.appendChild(p);
...
```

CONTOH 2

in HTML
```
...
<ul id="list"></ul>
...
```

in JS
```
...
// Data list
		const items = ["Item 1", "Item 2", "Item 3"];

		// Loop untuk membuat elemen HTML baru dan menambahkan konten
		for (let i = 0; i < items.length; i++) {
			// Membuat elemen HTML baru
			const li = document.createElement("li");

			// Menambahkan konten ke dalam elemen HTML baru
			li.innerHTML = items[i];

			// Menambahkan elemen HTML baru ke dalam list
			const list = document.getElementById("list");
			list.appendChild(li);
		}
...
```

SECTION 7

CONTOH 1

in HTML
```
...
<button id="tombol1">Tombol 1</button>
<button id="tombol2">Tombol 2</button>
...
```

in JS
```
...
// Menambahkan event listener untuk tombol 1
		const tombol1 = document.getElementById("tombol1");
		tombol1.addEventListener("click", function() {
			alert("Anda menekan tombol 1!");
		});

		// Menambahkan event listener untuk tombol 2
		const tombol2 = document.getElementById("tombol2");
		tombol2.addEventListener("click", function() {
			alert("Anda menekan tombol 2!");
		});
...
```

CONTOH 2

in HTML
```
...
<button id="tombol1">Klik untuk menambah</button>
<p id="hasil1">0</p>

<button id="tombol2">Klik untuk merubah warna latar belakang</button>
<p id="hasil2">Latar belakang saat ini: putih</p>
...
```

in JS
```
...
// Menambahkan event listener untuk tombol1
		const tombol1 = document.getElementById("tombol1");
		const hasil1 = document.getElementById("hasil1");
		let jumlah = 0;
		tombol1.addEventListener("click", function() {
			jumlah++;
			hasil1.innerHTML = jumlah;
		});

		// Menambahkan event listener untuk tombol2
		const tombol2 = document.getElementById("tombol2");
		const hasil2 = document.getElementById("hasil2");
		let warna = "putih";
		tombol2.addEventListener("click", function() {
			if (warna === "putih") {
				document.body.style.backgroundColor = "lightblue";
				hasil2.innerHTML = "Latar belakang saat ini: lightblue";
				warna = "lightblue";
			} else {
				document.body.style.backgroundColor = "white";
				hasil2.innerHTML = "Latar belakang saat ini: putih";
				warna = "putih";
			}
		});
...
```
