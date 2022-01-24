create database realestate;
use realestate;

create table branch
(
branchid varchar(10) not null primary key,
branchname varchar(30),
branchphone varchar(12),
branchadd varchar(40),
OpeningDate date
);

insert into branch values
('B101', 'Maju Sentosa', '0129835673', 'Lot 13, Jalan 4/12,Kuantan,Pahang', '2010-12-10'),
('B102', 'Maju Damai', '0122154365', 'Level 3 Jln Air Puteh,Ipoh,Perak', '2009-03-05'),
('B103', 'Aliran Maju', '0113219044', 'L1232 Jln Tun Razak,Pekan,Pahang', '2010-12-10');


create table employee
(
empid varchar(10) not null primary key,
empname varchar(30),
empphone varchar(12),
empdob date,
empadd varchar(40),
branchid varchar(10),
foreign key (branchid) references branch(branchid)
);

insert into employee values
('E101', 'Linda', '0123443991', '1980-10-12','No 21, JLn Damai 2,Kuantan,Pahang','B101'),
('E102', 'Jane', '0121212098', '1985-03-24','Lot 31, JLn 3/21B,Ipoh,Perak','B102'),
('E103', 'Ahmad', '0192132563', '1989-05-17','No 543, Lorong 13G,Ipoh,Perak','B102'),
('E104', 'Kumar', '0193213477', '1992-09-09','Lot 22, JLn Aman 14,Kuantan,Pahang','B101'),
('E105', 'Brian', '0118923123', '1994-12-11','No 17, JLn Peramu 2,Pekan,Pahang','B103'),
('E106', 'Shanti', '0132213477', '1987-11-23','No 212, JLn Makmur 2,Kuantan,Pahang','B101');

create table manager
(
EmpID varchar(10) not null primary key,
AppointedDate date,
EndDate date,
foreign key (empid) references employee(empid)
);

insert into manager values
('E101', '2010-12-28', '2016-12-28'),
('E104', '2016-12-28', '2020-12-28'),
('E103', '2010-12-28', '2015-12-28');


create table qualification
(
qualificationid varchar(10) not null primary key,
empid varchar(10),
level varchar(20),
qualificationname varchar(40),
dateobtain date,
foreign key (empid) references employee(empid)
);

insert into qualification values
('Q101', 'E101' , 'Bachelor','Bachelor of Finance', '2009-01-05'),
('Q102', 'E101' , 'Master', 'Master in Business Management','2016-12-24'),
('Q103', 'E102' , 'Bachelor', 'Bachelor of Finance','2007-10-12'),
('Q104', 'E103' , 'Bachelor', 'Bachelor of Real Estate','2000-07-15'),
('Q105', 'E104' , 'Bachelor', 'Bachelor of Real Estate','2005-08-19'),
('Q106', 'E105' , 'Bachelor','Bachelor in Business Management','2004-10-10'),
('Q107', 'E105' , 'Master', 'Master in Business Management','2010-09-05'),
('Q108', 'E106' , 'Bachelor', 'Bachelor of Finance','2060-06-13');

create table owner
(
ownerid varchar(10) not null primary key,
ownername varchar(30),
ownerphone varchar(12),
owneradd varchar(40),
ownerdob date
);

insert into owner values
('Own001', 'Azri', '0133343211', 'Lot 2,Jln 2/3,Kuantan,Pahang', '1980-12-11'),
('Own002', 'Rina', '0165478912', 'No 3,Jln Aman 2,Ipoh,Perak', '1979-03-21'),
('Own003', 'Jacky', '0116533498', '123,Lrg Permai Aman 2,Pekan,Pahang', '1990-05-14'),
('Own004', 'Lynn', '0121134887', 'Lot 1212,Jln Maju 2,Kuantan,Pahang', '1972-07-09'),
('Own005', 'Anand', '0142216577', 'No 37,Jln 13/25A,Kuantan,Pahang', '1987-03-21');



create table property
(
propid varchar(10) not null primary key,
empid varchar(10),
ownerid varchar(10),
propadd varchar(40),
propmarketvalue float,
propsellprice float,
propcompleteddate date,
foreign key (empid) references employee(empid),
foreign key (ownerid) references owner(ownerid)
); 


insert into property values
('P001', 'E101','Own001', '23,Jln 3/21,Kuantan,Pahang',150000,165000, '1980-12-23'),
('P002', 'E101','Own001', 'Lot 2235,Taman Indera,Berserah,Pahang',123000,135000, '1980-12-23'),
('P003', 'E102','Own002', '43, Blok 2,Jln 21/33B,Taiping,Perak',175000,190000, '1985-01-12'),
('P004', 'E102','Own003', '111,Jln Asarama 2/21 ,Ipoh,Perak',150000,165000, '1990-05-22'),
('P005', 'E103','Own004', '32B,Jln Dihilir 2/32A,Ipoh,Perak',210000,215000, '1985-07-23'),
('P006', 'E103','Own004', '42C,Jln Dihilir 1/42C,Ipoh,Perak',320000,328000, '2009-04-10'),
('P007', 'E103','Own004', 'Lot 14,Jln Harmoni 2/17 Ipoh,Perak',155000,165000, '1989-06-14'),
('P008', 'E104','Own005', 'Lot 2235,Taman Indera,Berserah,Pahang',224000,230000, '1992-11-17'),
('P009', 'E102','Own002', '34,Taman Mahkota,Kuantan,Pahang',215000,225000, '1998-09-13'),
('P0010', 'E105','Own001','Lot 2235,Jln Peramu 2/17,Pekan,Pahang',178000,185000, '1993-12-23'),
('P0011', 'E105','Own002','34,Lorong Ketapang 4A/22,Pekan,Pahang',192000,200000, '1997-10-19'),
('P0012', 'E104','Own005', '191,Jln Indera 12/4,Kuantan,Pahang',250000,265000, '2005-03-15');

create table listings
(
listingid varchar(10) not null primary key,
branchid varchar(10),
propid varchar(10),
listingdate date,
foreign key (branchid) references branch(branchid),
foreign key (propid) references property(propid)
);

insert into listings values
('L100', 'B101','P001', '2020-12-22'),
('L101', 'B101','P002', '2020-10-13'),
('L102', 'B102','P003', '2020-11-15'),
('L103', 'B102','P004', '2021-01-17'),
('L104', 'B102','P005', '2021-02-19'),
('L105', 'B102','P006', '2020-10-24'),
('L106', 'B102','P007', '2020-11-19'),
('L107', 'B101','P008', '2021-02-12'),
('L108', 'B101','P009', '2021-03-01'),
('L109', 'B103','P0010', '2020-12-06'),
('L1010', 'B103','P0011', '2021-02-15'),
('L111', 'B101','P0012', '2021-03-07');

commit;
