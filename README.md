# Tugas-2
?xml version="1.0" encoding="UTF-8"? untuk memulai pembuatan sintak xml
!DOCTYPE logbarang SYSTEM "logbarang.dtd" menyatakan bahwa dtd dengan logbarang sudah terhubung dengan xmlnya.
<logbarang> 
<barang>  
	<kode>M1112</kode>
 	<satuan>pc</satuan>  
 	<harga cur="nmtoken">5000</harga>  
	<asal>
		<pt>ladyrock</pt>   
		<kodewil>10</kodewil>  
	</asal>  
	<tujuan>   
		<pt>union</pt>   
		<kodewil>1001</kodewil>
	</tujuan> 
</barang>   

<barang>  
	<kode>M1122</kode>  
	<satuan>pc</satuan>  
	<harga cur="nmtoken">1000</harga>  
	<asal>   
		<pt>pbm</pt>   
		<kodewil>103</kodewil>  
	</asal>  
	<tujuan>   
		<pt>mitra kencana</pt>   
		<kodewil>300</kodewil>  
	</tujuan> 
</barang>   
</logbarang>



<?xml encoding="UTF-8"?>

<!ELEMENT logbarang (barang)+> 

<!ATTLIST logbarang
    xmlns CDATA #FIXED ''>

<!ELEMENT barang (kode?,satuan,harga,asal,tujuan)>
<!ATTLIST barang
    xmlns CDATA #FIXED ''>

<!ELEMENT kode (#PCDATA)>
<!ATTLIST kode
    xmlns CDATA #FIXED ''>

<!ELEMENT satuan (#PCDATA)>
<!ATTLIST satuan
    xmlns CDATA #FIXED ''>

<!ELEMENT harga (#PCDATA)>
<!ATTLIST harga
    cur CDATA #IMPLIED ''>

<!ELEMENT asal (pt,kodewil)>
<!ATTLIST asal
    xmlns CDATA #FIXED ''>

<!ELEMENT tujuan (pt,kodewil)>
<!ATTLIST tujuan
    xmlns CDATA #FIXED ''>

<!ELEMENT pt (#PCDATA)>
<!ATTLIST pt
    xmlns CDATA #FIXED ''>

<!ELEMENT kodewil (#PCDATA)>
<!ATTLIST kodewil
    xmlns CDATA #FIXED ''>>
    
//Pada elemen logbarang terdapat elemen barang dengan didalamnya terdapat element kode, satuan, harga, asal, dan tujuan. Dan pada elemen harga terdapat atribut 'cur = "nmtoken"'. Dalam elemen asal terdapat elemen pt dan kodewil dan dalam elemen tujuan terdapat elemen pt dan kodewil. Dan ditutup dengan elemen penutul barang. 
//Pada elemen kode diberi '?',tujuannya adalah agar tidak terjadi error apabila kodenya dihapus.
