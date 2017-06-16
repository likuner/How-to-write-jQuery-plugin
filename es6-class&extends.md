```javascript
calss Person {
    constructor(name,age) {
        this.name = name;
        this.age = age;
    }
    say() {
        console.info(`${this.name},${this.age}`);
    }
}

class Student extends Person {
    constructor(name,age,school) {
        super(name,age);
        this.school = school;
    }
    getSchool() {
        console.info(`${this.name},${this.age},${this.school}`);
    }
}

let stu = new Student('Peter', 18, 'No.2 high school');
stu.say();  //Peter,18 (extends from Person)
stu.getSchool();  //Peter,18,No.2 high school
```
