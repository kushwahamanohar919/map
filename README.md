# map  RXJS Angular

one Example
 ngOnInit(): void {

    let student = [
      { id: 123, name: "manohar", course: "MCA" },
      { id: 124, name: "mukesh kumar", course: "M.Tech" },
      { id: 125, name: "Anil", course: "B-Tech" },
      { id: 126, name: "khushi", course: "BA" },
    ];

    let studentObservable = from(student);

    studentObservable.pipe(map((item: any) => {
      return {
        name: item.name, id: item.id,
      }
    }), toArray()).subscribe(res => {
      console.log("student data", res);
    })



    let college = [
      { id: 123, name: "manohar", course: "MCA" },
      { id: 124, name: "Amita", course: "BA" },
      { id: 124, name: "harsh", course: "BA" },
    ];

    let COllObservable =from(college);
    COllObservable.pipe(map((item: any) => {
      return {
        id: item.id, name: item.name,
      }
    }), toArray()).subscribe(data => {
      console.log("student", data);
    })

  }
