Retrieve data spasial adalah sebuah kegiatan untuk melakukan select dan view data record dalam sebuah file dbf atau file shp baik itu berupa menampilkan titik, garis maupun polygon didalam sebuah geometri. Dalam menggunakannya data retrieve dapat dengan mudah digunakan menggunakan phyton karena didalam python sudah terdapat object object yang sudah terdaftar untuk data geospasial.

Tool yang dipakai bisa menggunakan lib pyshp

-   Melakukan select dan view

    Data record dari file dbf dan geometri dari file shp

    Cara retrieve data :

1.  Buka file nya

    -import shapefile

    -sf = shapefile.Reader(“nama.shp”)

2.  Menghitung jumlah Record

    File dbf :

    -sf.records() &gt; untuk menampilkan seluruh record nya

    -sf.record(n) &gt; untuk menampilkan satu record saja

    File shp :

    -sf.shapes() &gt; untuk menampilkan semuanya record

    -sf.shape(n) &gt; untuk menampilan satu record saja

    Atau bisa juga dengan -dir(shapes)

    Contoh menghitung records :

    a = sf.shapes()

    len(a)

    Contoh melihat nama fields

    Nama.file = sf.fields

    Print nama.fields

Membuat class di python

-vi gede.py

Import shapefile

Class gede(object) :

Defhitungbaris(self.namafile)

Sf = shapefile.Reader(namafile)

Record = sf.shapes()

Return len(rec)

-Import gede

-inst = gede.Gede()

-inst.hitungbaris(“loka/lokasi.shp”)
