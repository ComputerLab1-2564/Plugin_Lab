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


### 5. กำหนดที่ตั้งของไฟล์ต่างๆ
#### 5.1 ปัญหาที่จะเกิดขึ้นในการรันโปรแกรม

โดยปกติ Visual Studio จะสร้าง executable file ไว้ภายใต้ folder ของ project

ถ้าเรา build ทุก project จะพบว่าไฟล์ที่ได้จากการ  build จะอยู่คนละที่ ทำให้ไม่สามารถรันได้

![image](https://user-images.githubusercontent.com/567256/142582866-57b5d041-9322-4457-aed8-e14dd89e9ff4.png)




