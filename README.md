# Jarkom-modul-4-b09-2022-

### Anggota Kelompok
| Nama                 | NRP        |
|----------------------|------------|
| Gery Febrian Setyara | 5025201151 |
| Muhammad Yunus       | 5025201171 |
| Hafiz Kurniawan      | 5025201032 |

## Persiapan
Topologi jaringan

![soal shift 4 1](https://user-images.githubusercontent.com/92217354/204081808-d0ddbc82-0d19-4b21-b530-5abd86528e24.png)

## Pembagian Subnet

![Subenet-Circle](https://user-images.githubusercontent.com/92217354/204081922-3fb26f47-1837-4134-a845-9e9521612435.png)


## VLSM
Pertama-tama kita melakukan perhitungan pada IP nya terlebih dahulu


|Subnet|Alias  | Jumlah IP  | Length |
|------|-------|------------|--------|
|  A1  |Guideau-The Minister|1001|/22|
|  A2  |Johan-Panora-The Dauntless|251|/24|
|  A3  |The Dauntless-The Minister|2|/30|
|  A4  |The Order-The Minister|2|/30|
|  A5  |The Order-Ashaf|51|/26|
|  A6  |The Order-The Resonance|2|/30|
|  A7  |The Magical-The Resonance|2|/30|
|  A8  |Haines-Corvext-The Magical|271|/23|
|  A9  |The Resonance-The Instrument|2|/30|
|  A10  |Matt Cugat-The Instrument|121|/25|
|  A11  |The Instrument-The Profound|2|/30|
|  A12  |The Profound-Spendrow|121|/25|
|  A13  |The Profound-Helga|71|/25|
|  A14  |The Firefist-The Instrument|2|/30|
|  A15  |The Firefist-Oakleave|501|/23|
|  A16  |The Firefist-Keith-The Queen|212|/24|
|  A17  |The Queen-The Witch|2|/30|
|  A18  |The Beast-The Resonance|2|/30|
|  Total |                       |2618|/20|


## Pohon IP
Dilakukan pembagian subnet dengan Pohon IP,disini kami memilih yang paling kiri sehingga IP paling efisien

![VLSM-B09](https://user-images.githubusercontent.com/92217354/204082631-0d817765-4033-47e0-a97f-36fb2accc9d1.png)


## Hasil Pembagian IP
|Subnet|Node  | IP       |Submet Mask  |Length |
|------|------|----------|-------------|-------|
| A1   |The Minister|192.177.0.1|255.255.252.0|/22  |
|      |Guideau|192.177.0.2|255.255.252.0|/22  |
| A2   |The Dauntless|192.177.8.1|255.255.255.0|/24  |
|      |Johan|192.177.8.2|255.255.255.0|/24  |
|      |Phanora|192.177.8.2|255.255.255.0|/24  |
| A3   |The Minister|192.177.11.193|255.255.255.252|/30  |
|      |The Dauntless|192.177.11.194|255.255.255.252|/30  |
| A4   |The Minister|192.177.11.198|255.255.255.252|/30  |
|      |The Order|192.177.11.197|255.255.255.252|/30  |
| A5   |The Order|192.177.11.129|255.255.255.192|/26  |
|      |Ashaf|192.177.11.130|255.255.255.192|/26  |
| A6   |The Order|192.177.11.201|255.255.255.252|/30  |
|      |The Resonance|192.177.11.202|255.255.255.252|/30  |
| A7   |The Magical|192.177.11.206|255.255.255.252|/30  |
|      |The Resonance|192.177.11.205|255.255.255.252|/30  |
| A8   |The Magical|192.177.4.1|255.255.254.0|/23  |
|      |Coverxt|192.177.4.2|255.255.254.0|/23  |
|      |Haines|192.177.4.3|255.255.254.0|/23  |
| A9   |The Instrument|192.177.11.210|255.255.255.252|/30  |
|      |The Resonance|192.177.11.209|255.255.255.252|/30  |
| A10   |Matt Cugat|192.177.10.2|255.255.255.128|/25  |
|      |The Instrument|192.177.10.1|255.255.255.128|/25  |
| A11   |The Instrument|192.177.11.213|255.255.255.252|/30  |
|      |The Profound|192.177.11.214|255.255.255.252|/30  |
| A12   |Spendrow|192.177.10.130|255.255.255.128|/25  |
|      |The Profound|192.177.10.129|255.255.255.128|/25  |
| A13   |Helga|192.177.11.2|255.255.255.128|/25  |
|      |The Profound|192.177.11.1|255.255.255.128|/25  |
| A14   |The Instrument|192.177.11.217|255.255.255.252|/30  |
|      |The Firefist|192.177.11.218|255.255.255.252|/30  |
| A15   |Oakleave|192.177.6.2|255.255.254.0|/23  |
|      |The Firefist|192.177.6.1|255.255.254.0|/23  |
| A16   |The Firefist|192.177.9.1|255.255.255.0|/24  |
|      |The Queen|192.177.9.3|255.255.255.0|/24  |
|      |Keith|192.177.9.2|255.255.255.0|/24  |
| A17   |The Queen|192.177.11.221|255.255.255.252|/30  |
|      |The Witch|192.177.11.222|255.255.255.252|/30  |
| A18   |The Beast|192.177.11.226|255.255.255.252|/30  |
|      |The Resonance|192.177.11.225|255.255.255.252|/30  |


## Modules
Perlu menambahkan module NM-2FE2W agar Router dapat Ngelink lebih banyak

![image](https://user-images.githubusercontent.com/92217354/204083866-a437961b-a0ea-4004-8d8b-790809086ba0.png)

## Routing
Perlu dilakukan Routing untuk tiap router agar dapat terhubung dari satu dengan yang lain

- The Minister

Dalam The Minister akan mengambil semua dari Guideau,The Dauntless,The Order

![The Minister](https://user-images.githubusercontent.com/92217354/204083953-b320c100-83ac-4406-964e-6ed86467b5f5.jpeg)

- The Dauntless

Dalam The Dauntless akan mengambil semua dari The Minister dan Phanora dan Johan

![The Dauntless](https://user-images.githubusercontent.com/92217354/204084027-596d8287-773c-4d71-8ed5-04817562857a.jpeg)


- The Order 

Dalam The Order akan Mengambil Semua dari The Resonance,Guideau,dan Semua Ip 192.177.8.0(Johan,Phanora)

![image](https://user-images.githubusercontent.com/92217354/204084176-7d3a2cd1-a6ca-410f-886b-50be9b3ca1d7.png)

- The Resonance
Dalam The Resonance akan Mengambil Semua dari The Order,The Instrument,dan Semua IP 192.177.4.0(Haines,Corvext)

![The Resonance](https://user-images.githubusercontent.com/92217354/204084223-7ddff67b-621a-4f99-90f4-2c6e4705a224.jpeg)

- The Magical
Dalam The Magical akan mengambil semua dari The Resonance

![The Magical](https://user-images.githubusercontent.com/92217354/204084253-25bead5f-dfe8-48df-9774-d3f1a570b1f6.jpeg)

- The Instrument
Dalam The Instrument akan mengambil semua dari The Profound,The Resonance,Keith,Oakleave

![The Instrument](https://user-images.githubusercontent.com/92217354/204084290-966961c1-c914-4372-8fa9-3700adce6813.jpeg)

- The Profound
Dalam The Profound akan mengambil semua dari The Instrument

![The Profound](https://user-images.githubusercontent.com/92217354/204084313-aab02a5f-f616-4a17-a50f-5dfa21046c01.jpeg)

- The Firefist
Dalam The Firefist akan mengambil semua dari The Instrument dan dari The Queen 

![The Firefist](https://user-images.githubusercontent.com/92217354/204084352-385a5cee-3f68-4cd7-8252-072921b06746.jpeg)

- The Queen
Dalam The Queen akan mengambil semua dari The Firefist

![The Queen](https://user-images.githubusercontent.com/92217354/204084384-381505d6-4eee-4101-b861-f19370370218.jpeg)


## CIDR

## Topology GNS3

![image](https://user-images.githubusercontent.com/92217354/204084687-8c740708-b5e9-404d-a523-d8939d0a30aa.png)



## Kesulitan Yang Dihadapi

- Waktu perhitungan yang cukup lama karena tidak yakin perhitungan benar
- Kurang Waktu
