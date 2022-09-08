# todo-with-constructor

todo simples, fixando a criação de tasks a partir dum metodo constructor.

```js

function Task(name, completed, createdAt, updatedAt) {
    if (!name) {
      throw new Error("Name is required.");
    }

    let _name = name;
    
    this.completed = completed || false;
    this.createdAt = createdAt || Date.now();
    this.updatedAt = updatedAt || null;
    this.toggleDone = function () {
      this.completed = !this.completed;
    };
    this.getName = function () {
      return _name;
    };
    this.setName = function (name) {
      _name = name;
      this.updatedAt = Date.now();
    };
  }


```

![image](https://user-images.githubusercontent.com/75024157/189232584-b6737ab8-4773-49eb-ac72-a4f0e8a73d95.png)
