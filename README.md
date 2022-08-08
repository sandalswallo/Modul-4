###### Nama : Ferdy Aridho Irawan
###### Kelas : RPL 1
###### Absen : 27
## Modul 4
### View Blade Template

1. Buka file projectmu
2. pilih resources-->view
3. Pada view ini buat folder baru dengan nama barang,kategori, dan layout
4. Setelah itu buat file lagi di dalam file barang,kategori, dan layout
  
   -buat file baru didalam file barang dengan nama = home.blade.php
   
   -buat file baru didalam file kategori dengan nama = index.blade.php
  
   
   -buat file baru didalam file barang dengan nama = app.blade.php
   
   ![image](https://user-images.githubusercontent.com/109930428/183352636-f8172aa9-856e-46c4-b2c4-edef4023dfe7.png)
   
   
 5. Buka file app.blade.php 
 6. Di dalam file app.blade.php kita masukkan codingan navbar, css, dan juga js. Codingan navbar, css, dan js akan kita ambil dari bootstrap
 
 ![image](https://user-images.githubusercontent.com/109930428/183353114-e4e61d7d-c8a8-4baf-ba86-250a55f0bed5.png)
 
 file atau link css dari bootstrap
 
 ![image](https://user-images.githubusercontent.com/109930428/183353316-809dc390-0636-41d5-ab18-4e92c542017f.png)

file atau link js dari bootstrap

![image](https://user-images.githubusercontent.com/109930428/183354639-16b1b266-535c-40d0-98d6-cb63057d3776.png)

file atau link navbar dari bootstrap

 7. Setelah dapat file navbar, css, dan js dari bootstrap kita akan menyusunnya pada file app.blade.php seperti dibawah ini!

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
    <title>
        @yield('title')
    </title>
</head>
<body>


{{--untuk navbar--}}
   <div class="container">

   <nav class="navbar navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand " href="#">penjualan</a>

    <button class="navbar-toggler" type="button" 
    data-bs-toggle="collapse" 
    data-bs-target="#navbarSupportedContent" 
    aria-controls="navbarSupportedContent" 
    aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link " href="/kategori">kategori</a>
        </li>
        <li class="nav-item">
          <a class="nav-link " href="/barang">barang</a>
        </li>
  
    </div>
      </div>
         </nav>
             </div>

   {{--conten--}}
   <div class="container">
    @yield('content')
   </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>  
</body>
</html>
```


8.Buka file home.blade.php pada folder barang lalu masukkan codingan dibawah ini!
```
@extends('layout.app')

@section('title')
barang
@endsection
@section('content')
<div class ="mt-3">
<table class="table table-striped">
     <thead>
        <tr>
            <th width="5%">No.</th>
            <th>Nama Barang</th>
            <th width="20%">Kategori</th>
            <th width="10%">QTY</th>
            <th width="15%">Harga Beli</th>
            <th width="15%">Harga Jual</th>
            <th>Aksi</th>
        </tr>
     </thead>

     <tbody>
      <tr>
        <td>1</td>
        <td>Kursi</td>
        <td>ATK</td>
        <td>10</td>
        <td>Rp.15.000</td>
        <td>Rp.20.000</td>
        <td>Hapus | Edit</td>
      </tr>

      <tr>
        <td>2</td>
        <td>Meja</td>
        <td>ATK</td>
        <td>14</td>
        <td>Rp.25.000</td>
        <td>Rp.35.000</td>
        <td>Hapus | Edit</td>
      </tr>

     </tbody>

    
    </table>
</div>
@endsection
```

9. Lalu buka juga file index.blade.php pada folder kategori copy codingan yang ada pada file home.blade.php ,lalu kita rubah sedikit sintax di yang ada pada codingan home.blade.php seperti dibawah ini!

```
@extends('layout.app')

@section('title')
kategori
@endsection
@section('content')
<div class ="mt-3">
    <table class="table table-striped">
     <thead>
        <tr>
            <th width="5%">No.</th>
            <th>Nama</th>
            <th width="10%">Aksi</th>
        </tr>
     </thead>

     <tbody>
      <tr>
        <td>1</td>
        <td>ATK</td>
        <td>Hapus | Edit</td>
      </tr>

     </tbody>

    
    </table>
</div>
@endsection

```
