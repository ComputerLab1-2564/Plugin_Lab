# Plugin dev laboratory

ขั้นตอนการทดลอง 
### 1. clone repository นี้
```git
  git clone https://github.com/ComputerLab1-2564/Plugin_Lab.git
```
### 2. clone submodule

```git
  cd Plugin_Lab 
  git submodule update --init --recursive
```

### 3. เปลี่ยนเข้าไปใน folder ที่ชื่อ ```PlugInLab```
 
![image](https://user-images.githubusercontent.com/567256/142580905-692dd9e8-02ce-4440-9fe9-700756b2793a.png)


### 4. เปิด project  ด้วย Visual Studio

Double click ที่ไฟล์ ```PluginLab.sln``` จะเป็นการเรียก Visual Studio ขึ้นมา (ในตัวอย่างนี้ใช้รุ่น 2019 Community)

![image](https://user-images.githubusercontent.com/567256/142581181-0ac00c7b-130a-4b76-b80b-220dda888810.png)

### 5. ปรับแก้ properties ของทุก project ให้ตรงกัน

![image](https://user-images.githubusercontent.com/567256/142581545-49540087-ecdd-4e2e-9c74-6e54cab6b1aa.png)

|No| รายการที่ต้องทำ |
|--|--------------|
|1 | คลิกขวาที่ชื่อ project เลือกเมนูย่อย Properties |
|2 | เลือกแท็บ Application |
|3 | เลือก Tagget framework ให้ตรงกับที่ติดตั้งไว้ในเครื่องคอมพ์ของเรา |


### 6. กำหนดที่ตั้งของไฟล์ต่างๆ
#### 6.1 ปัญหาที่จะเกิดขึ้นในการรันโปรแกรม

โดยปกติ Visual Studio จะสร้าง executable file ไว้ภายใต้ folder ของ project

ถ้าเรา build ทุก project จะพบว่าไฟล์ที่ได้จากการ  build จะอยู่คนละที่ ทำให้ไม่สามารถรันได้

![image](https://user-images.githubusercontent.com/567256/142582866-57b5d041-9322-4457-aed8-e14dd89e9ff4.png)

#### 6.2 กำหนด folder ปลายทางสำหรับการ build แต่ละ project

เพื่อให้โปรแกรมของเราสามารถทำงานได้ ให้สร้าง folder ชื่อ MyApplication ไว้ที่ root ของ Folder ของ repository ตามโครงสร้างดังรูปนี้

![image](https://user-images.githubusercontent.com/567256/142584333-d9b62b29-9c50-4a02-b13b-e825879b4065.png)

#### 6.3 กำหนด properties ของแต่ละ project

![image](https://user-images.githubusercontent.com/567256/142584820-842167aa-274c-446f-93c5-fe873324f1a0.png)

|No| รายการที่ต้องทำ |
|--|--------------|
|1 | เลือกแท็บ Application |
|2 | กด Browse... เพื่อเลือกที่ตั้งของ output file  ดังตารางด้านล่าง|


ตารางแสดงที่ตั้งของ output file ของแต่ละ project
|Project name| Output path |
|--|--------------|
| Host | MyApplication |
| PluginInterface | MyApplication   |
| Plugin1 | MyApplication\Plugins   |
| Plugin2 | MyApplication\Plugins   |
| Plugin... | MyApplication\Plugins |
| Plugin4 | MyApplication\Plugins   |


### 7. Build โปรเจคต่างๆ  
 
Build โปรเจคต่างๆ ให้ครบ ถ้ามี error  ให้แก้ไขจนถูกต้อง

Plugin ต่างๆ จะมีรูปแบบเป็นไฟล์ dll และในการทดลองนี้จะมีเพียงโปรเจคเดียวคือ Host  เท่านั้นที่สามารถเรียกรันได้

การกำหนดโปรเจค Host เป็น Startup project (กรณีที่ยังไม่ได้เป็น) ทำได้ดังรูปด้านล่างนี้

![image](https://user-images.githubusercontent.com/567256/142585444-d13d45da-0da6-4356-87b1-9f087b8869b0.png)




# Happy developing... #

(not happy ending)
