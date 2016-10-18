# Chapter-6
CREATE TABLE dept_emp (
    emp_no INT(11) PRIMARY KEY NOT NULL,
    dept_no char(4) PRIMARY KEY NOT NULL,
    from_date date NOT NULL,
    to_date date NOT NULL,
    FOREIGN KEY (emp_no) REFERENCES employees(emp_no),
    FOREIGN KEY (dept_no) REFERENCES departments(dept_no)
  );

  CREATE TABLE titles (
    emp_no INT(11) PRIMARY KEY NOT NULL,
    title varchar(50) PRIMARY KEY NOT NULL,
    from_date date PRIMARY KEY NOT NULL,
    to_date date DEFAULT NULL,
    FOREIGN KEY (emp_no) REFERENCES employees(emp_no)
  );
