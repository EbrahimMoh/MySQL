create database Insurance;
use Insurance;
create table User(
user_ID varchar(10),
name varchar(50),
phoneNum int ,
email varchar(50),
Address varchar(50),
primary key (user_ID)
);
create table Car (
user_ID varchar(10),
Car_ID int,
plateNum varchar(50),
Car_model varchar(50),
Car_color varchar(50),
License varchar(50),
primary key (car_ID),
FOREIGN KEY (user_ID) REFERENCES User (user_ID)
);
create table Motorcycle (
user_ID varchar(10),
Motor_ID int,
plateNum varchar(50),
Motor_model varchar(50),
Motor_color varchar(50),
License varchar(50),
primary key (motor_ID),
FOREIGN KEY (user_ID) REFERENCES User (user_ID)
 
);
create table Travel (
user_ID varchar(10),
Travel_ID varchar(10),
CoverType varchar(50),
destination varchar(50),
travellerType varchar(50),
Date varchar(20),
primary key (travel_ID),
FOREIGN KEY (user_ID) REFERENCES User (user_ID)
);
create table Home (
user_ID varchar(10),
Home_ID varchar(20),
address varchar (50),
Coveragedate varchar(10),
buildingType varchar(50),
constructionType varchar(50),
amount varchar(10),
primary key (home_ID),
foreign key (user_ID) references User (user_ID)
);
 create table Health (
user_ID varchar(10),
health_ID varchar(10),
city varchar(50),
state varchar(50),
dateOFBirth varchar(20),
facility_name varchar(50),
primary key (health_ID),
foreign key (user_ID) references User (user_ID)
);
create table Payment (
user_ID varchar(10),
amount float (6,2),
foreign key (user_ID) references User (user_ID)
);
create table Accident (
user_ID varchar(10),
accident_ID varchar (10),
reportNum int,
location varchar(50),
date varchar(20),
primary key(accident_ID),
foreign key (user_ID) references User (user_ID)
);
 
 
create table Student (
user_ID varchar(10),
student_ID varchar(10),
institution_name varchar(50),
city varchar(50),
state varchar(50),
primary key (student_ID),
foreign key (user_ID) references User (user_ID)
);

INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Abu”, “abu@gmail.com”, “A3568”, “012345678”, “Maran,Pahang”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Alif”, “alif@gmail.com”, “A4127”, “012435875”, “Kota Bharu, Kelantan”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Hafiz”, “hafiz@gmail.com”, “A8765”, “015639465”, “Ipoh,Perak”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Shahrul”, “shahrul@gmail.com”, “A9876”, “0157935549”, “Kuantan, Pahang”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Ibrahim”, “ibrahim@gmail.com”, “A0987”, “016382956”, “Pekan, Pahang”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Khalis”, “khalis@gmail.com”, “A5637”, “017495275”, “Taiping, Perak”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Jiha”, “jiha@gmail.com”, “A8435”, “017529454”, “Kemaman, Terengganu”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Amira”, “amira@gmail.com”, “A7623”, “015349663”, “Gambang, Pahang”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Fatihah”, “fatihah@gmail.com”,  “A0612”, “016435696”, “Segamat,Johor”);
INSERT INTO User (name, email, user_ID, phoneNum, address) VALUES (“Siti”, “siti@gmail.com”, “A8769”, ”016539264”, “Georgetown,Penang”);

INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A3568”, “826472”, “CAD8967”, “Perodua”, “White”, “P”);
INSERT INTO Car (user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A4127”, “739462”, “DSA1234”, “Honda”,”White”, “P”);
INSERT INTO Car (user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A8765”, “473057”, “ADE8906”, “Toyota”, “Black”, “P”);
INSERT INTO Car (user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A9876”, “27437”, “CDA4789”, “Peugeot”, “Brown”, “P”);
INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A0987”, “364820”, “CAA5476”, “Honda”, “White”, “P”);
INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A5637”, “573629”, “ACB5234”, “Toyota”, “Black”, “P”);
INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A8435”, “428837”, “TBB1768”, “Proton”, “Gray”, “P”);
INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A7623”, “213837”, “CBE9074”, “Perodua”, “Gray”, “P”);
INSERT INTO Car (user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A0612”, “695732”, “JKA3755”, “Mitsubishi”, “Black”, “L”);
INSERT INTO Car ( user_ID, Car_ID, plateNum, Car_model, Car_color, License) VALUES (“A8769”, “063278”, “PKA6523”, “Honda”, “White”, “L”);

INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A3568”, “84369”, “CD4023”, “Yamaha”, “Red”, “B1”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A4127”, “74962”, “DD6789”, “Honda”, “Blue”, “B”);
INSERT INTO Motorcycle ( user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES ( “A8765”, “75278”, “ABC3425”, “Suzuki”, “White”, “B”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A9876”, “92714”, “CB2525”, “Honda”, “Black”, “B1”);
INSERT INTO Motorcycle ( user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES ( “A0987”, “52801”, “CB5622”, “Aprilia”, “Gray”, “B”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES ( “A5637”, “59624”, “AB4632”, “Kawasaki”, “White”, “B”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A8435”, “82481”, “TR6309”, “SYM”, “White”, “B”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A7623”, “59725”, “CC5930”, “Yamaha”, “Black”, “B”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A0612”, “60626”, “JP4252”, “Suzuki”, “Red”, “B1”);
INSERT INTO Motorcycle (user_ID, Motor_ID, plateNum, Motor_model, Motor_color, License) VALUES (“A8769”, “50025”, “PT6901”, “Modenas”, “Black”, “B”);

INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A3568”, “AB75L”, “Trip cancellation”, “Madagascar”, “Business”, “13th May 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A4127”, “TG25G”, “Trip cancellation”, “Africa”, “Expedition”, “14th June 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A8765”, “HT25H”, “baggage”, “Cuba”, “Expedition”, “25th May 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A9876”, “TN45S”, “Medical assistant”, “Korea”, “Holiday”, “21st May 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A0987”, “UJ35H”, “Trip cancellation”, “Bahrain”, “Business”, “21st April 2021”);
INSERT INTO Travel ( user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A5637”, “SG25E”, “Baggage”, “China”, “Business”, “31st March 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A8435”, “HG09U”, “Trip cancellation”, “Japan”, “Business”, “14th March 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A7623”, “HF42J”, “Accidental death”, “Selangor”, “Holiday”, “28th April 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A0612”, “RR45L”, “Accidental death”, “Terengganu”, “Holiday”, “17th June 2021”);
INSERT INTO Travel (user_ID, Travel_ID, coverType, destination, TravellerType, Date) VALUES (“A8769”, “NV23P”, “Baggage”, “Sri Lanka”, “Holiday”, “5th June 2021”);

INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A3568”, “JRW VF 1472 C”, “Maran, Pahang”, “2021-08-23”, “Condominium”, “Frame”, “100000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A4127”, “NWU BY 1974 M”, “Kota Bharu, Kelantan”, “1 year”, “Apartment”, “Fire Resistant”, “50000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A8765”, “NWI UR 2973 K”, “Ipoh, Perak”, “1 year”, “Terrace”, “Heavy timber”, “50000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A9876”, “DVE WD 1276 L”, “Kuantan, Pahang”, ”1 year”, “Bungalow”, “Heavy timber”, “100000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A0987”, “NSM OL 1074 H”, “Pekan, Pahang”, “1 year”, “Bungalow”, “Frame”, “100000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A5637”, “RHK RG 2846 J”, “Taiping, Perak”, “1 year”,  “Two-storey bungalow”, “Frame”, “100000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A8435”, “JOQ UJ 3462 K”, “Kemaman, Terengganu”, “1 year”, “Bungalow”, “Frame”, “100000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A7623”, “ASN HN 1987 L”, “Gambang, Pahang”, “1 year”, “Condominium”, “Frame”, “50000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A0612”, “TNW TG 6274 V”, “Segamat, Johor”, “1 year”, “Terrace”, “Fire resistant”, “50000”);
INSERT INTO Home (user_ID, Home_ID, address, Coveragedate, buildingType, constructionType, amount) VALUES (“A8769”, “SNE CT 1318 R”, “Georgetown, Penang”, “1 year”, “Apartment”, “Fire Resistant”, “50000”);

INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A3568”, “00AB1234”, “Maran”, “Pahang”, “Blood banks”, “23/5/1970”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A4127”, “19BY1387”, “Kota Bharu”, “Kelantan”, “Surgical”, “13/2/1988”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A8765”, “47SJ1083”, “Ipoh”, “Perak”, “Surgical”, “12/10/1987”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A9876”, “48FW0649”, “Kuantan”, “Pahang”, “Blood banks”, “1/9/1997”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A0987”, “95RS8164”, “Pekan”, “Pahang”, “Surgical”, “8/8/1990”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A5637”, “02JN2379”, “Taiping”, “Perak”, “Surgical”, “13/2/1990”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A8435”, “58NS9301”, “Kemaman”, “Terengganu”, “Surgical”, “7/6/1994”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A7623”, “17PJ1949”, “Gambang”, “Pahang”, “Blood banks”, “9/10/1992”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A0612”, “61NE2691”, “Segamat”, “Johor”, “Blood banks”, “8/12/1993”);
INSERT INTO Health (user_ID, Health_ID, city, state, Facility_name, dateOfBirth) VALUES (“A8769”, “00AN1655”, “Georgetown”, “Penang”, “Blood banks”, “6/6/1999”);

INSERT INTO Payment ( user_ID, amount) VALUES (“A3568”, “1000”);
INSERT INTO Payment (user_ID, amount) VALUES ( “A4127”, “1000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A8765”, “2000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A9876”, “3000”);
INSERT INTO Payment (user_ID, amount) VALUES ( “A0987”, “4000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A5637”, “2000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A8435”, “3000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A7623”, “5000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A0612”, “3000”);
INSERT INTO Payment (user_ID, amount) VALUES (“A8769”, “5000”);

INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A3568”, “U492930”, “827201”, “Johor”, “30th February 2021”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A4127”, “B038286”, “181085”, “Kelantan”, “4/5/2008”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A8765”, “K827520”, “149157”, “Ipoh”, “4/4/2012”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A9876”, “K032895”, “816902”, “Selangor”, “15/7/2013”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A0987”, “F388202”, “254719”, “Selangor”, “9/4/2008”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A5637”, “O937820”, “201735”, “Penang”, “16/9/2015”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A8435”, “P932758”, “238567”, “Pahang”, “6/3/2007”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A7623”, “B929495”, “245183”, “Penang”, “6/8/2013”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A0612”, “I832590”, “988280”, “Kedah”, “7/12/2012”);
INSERT INTO Accident (user_ID, Accident_ID, reportNum, location, date) VALUES (“A8769”, “D909999”, “766810”, “Perlis”, “8/8/2017”);

INSERT INTO Student (user_ID, Student_ID, institution_name, city, state) VALUES (“A3568”, “91770021”, “uniMAP”, “Arau”, “Perlis”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A4127”, “09184902”, “uniMAP”, “Arau”, “Perlis”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A8765”, “AC92815”, “USM”, “Nibong Tebal”, “Penang”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A9876”, “CB20078”, “UMP”, “Pekan”, “Pahang”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A0987”, “CA20133 “, “UMP”, “Pekan”, “Pahang”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A5637”, “CB20118”, “UMP”, “Pekan”, “Pahang”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A8435”, “CB20120”, “UMP”, “Pekan”, “Pahang”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A7623”, “85672JE”, “UKM”, “Bangi”, “Selangor”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A0612”, “0016482780”, “UUM”, “Sintok”, “Kedah”);
INSERT INTO Student (user_ID, Student_ID, Institution_name, city, state) VALUES (“A8769”, “26876618”, “uniMAP”, “Arau”, “Perlis”);








