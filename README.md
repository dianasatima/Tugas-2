# Tugas-2
<?xml version="1.0" encoding="UTF-8"?> //untuk memulai pembuatan sintak xml
<!DOCTYPE logbarang SYSTEM "logbarang.dtd"> //menyatakan bahwa dtd dengan logbarang sudah terhubung dengan xmlnya.
<<logbarang> 
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
</logbarang>>



<<?xml encoding="UTF-8"?>

<!ELEMENT logbarang (barang)+> //Dalam element dtd logbarang terdapat element dengan nama "barang". Terdapat tanda "+" ini menyatakan bahwa data pada element barang harus ada minimal 1 atau lebih.
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
