### Làm việc với nhánh branch tạo nhánh gộp nhánh trong Git

**Khởi tạo dự án với commit**

```
$ git init                      #khởi tạo Repo
$ touch 0.txt                   #Tạo một file mới trong thư mục làm việc
$ git add .                     #đưa vào stage
$ git commit -m"C0"             #commit

$ touch 1.txt
$ git add .
$ git commit -m"C1"

$ touch 2.txt
$ git add .
$ git commit -m"C2"
```

**Lịch sử commit**

```
$ git log --pretty=oneline
```

![image](https://user-images.githubusercontent.com/69178270/147456563-b2ee0c3d-d674-4be1-9b2f-c752dd65c1ef.png)

**Xem danh sách các nhánh - branch**

```
$ git branch
* master
```

Có một nhánh là master, ký hiệu * cho biết đây là nhánh hiện tại

**Tạo một nhánh mới**

```
$ git branch alpha
```

**Chuyển nhánh làm việc mới**

```
$ git checkout alpha
```

![image](https://user-images.githubusercontent.com/69178270/147456992-7924fccb-77b5-4006-ac2e-80d204ab0ec2.png)

**Thực hiện commit trên nhánh mới**

```
$ touch 3.txt                   #Tạo một file mới trong thư mục làm việc
$ git add .                     #đưa vào stage
$ git commit -m"C4"   
```

![image](https://user-images.githubusercontent.com/69178270/147457132-11862ef2-9deb-47e3-a77f-6643bfbec038.png)

**Tiếp tục tạo sự thay đổi và commit trên nhánh alpha**

```
$ echo "Update new content to file" > 1.txt  #thêm nội dung mới vào file 1.txt
$ git add .
$ git commit -m"C4"
```

**Chuyển về làm việc với nhánh master**

```
git checkout master
```

**Tạo sự thay đổi và commit cho nhánh master**

```
$ touch 4.txt
$ echo "Update code" > 0.txt
$ git add .
$ git commit -m"C5"
```

**Tiếp tục tạo nhánh mới rẽ từ master**

```
$ git branch sualoigap              #tạo nhánh
$ git checkout sualoigap    
```

**Tạo sự thay đổi và commit trên nhánh sualoigap**

```
$ echo "Sua loi tren 2.txt" > 2.txt
$ git add .
$ git commit -m"C6"
```

**Xem lại lịch sử commit sualoigap**

```
$ git log --pretty=oneline
```

```
$ echo "Sua loi tren 1.txt" > 1.txt
$ git add .
$ git commit -m"C7"
```

**Trộn nhánh sualoigap vào nhánh master**

```
$ git checkout master               #tạo nhánh
$ git merge sualoigap               #hợp nhất
```

![image](https://user-images.githubusercontent.com/69178270/147459035-8545ce2d-f97f-42a6-aeeb-2df81e0e8220.png)

**xóa nhánh sualoigap**

```
$ git branch -d sualoigap
$ git branch
  alpha
* master
```

**Xử lý xung đột khi gộp nhánh**

Lấy 7 ký tự đầu trong SHA của c2 tại giao đoạn chứa phân nhánh

```
$ git checkout 0d7ae45f          #0d7ae45f là hash của commit C2
HEAD is now at 0d7ae45 C2
```

![image](https://user-images.githubusercontent.com/69178270/147459938-9afc511f-3508-4403-9abb-0484388c1e99.png)

Quay lại thời điểm snapshot C2

```
$ git checkout alpha
```

```
$ git checkout master
```

kiểm tra sung đột

![image](https://user-images.githubusercontent.com/69178270/147460089-16881820-ab79-4c92-a39f-e20848803de5.png)

**Gộp nhánh alpha vào master**

```
$ git checkout master
$ git merge alpha       #gộp nhánh
Auto-merging 1.txt
CONFLICT (content): Merge conflict in 1.txt
Automatic merge failed; fix conflicts and then commit the result.
```

**xử lý xung đột khi gộp nhánh**

