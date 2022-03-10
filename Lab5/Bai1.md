### Giải thích giá trị từ khóa ‘this’ trong JavaScript! Minh họa lời giải thích của bạn
**bằng một ví dụ!**

# Trường hợp gọi hàm global
Từ khóa **this** trong Javascript chỉ đối tượng đã gọi hàm cụ thể xem ví dụ bên dưới:

    function logger() {
        console.log(this);
    }

    logger(); 

**Output: Đối tượng window** bởi vì mặc định khi gọi hàm nếu không có đối tượng đứng trước đó thì nó sẽ mặc định là đối tượng **window**

# Trường hợp sử dụng đối tượng để gọi tới hàm
    const user1 = {
        name: "Đào Đức Minh Khôi",
        age: 19,
        getInfo: function() {
            console.log(this);
        }
    }

    user1.getInfo();

**Output: Trả về đối tượng user1**

# Trường hợp sử dụng đối tượng là 1 biến global
    var ten = "Đào Đức Minh Khôi"

    console.log(this.ten); 
**Output: Từ khóa 'this' ở đây tượng trưng cho đối tượng window**

# Trường hợp sử dụng this trong class 
     class User {
        constructor(name, age) {
          this.name = name;
          this.age = age;
        }

        getInfo() {
          console.log(this);
        }
      }

      const DaoKhoi = new User("Đào Đức Minh Khôi", 20);
      DaoKhoi.getInfo();
**Output: Từ khóa 'this' ở đây tượng trưng cho đối tượng gọi hàm getInfo**



