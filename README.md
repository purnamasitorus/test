-- Create a database called record_company and select this database for querying
CREATE DATABASE record_company; #Creates a new database called "record_company1"
USE record_company; #chooses the database schema we would like to query

-- Create table for bands
CREATE TABLE bands (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  PRIMARY KEY (id)
);

-- Create table for albums. Notice its relationship with bands table.
CREATE TABLE albums (
  id INT NOT NUL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  release_year INT,
  band_id INT NOT NULL,
  PRIMARY KERY (id),
  FOREIGN KEY (band_id) references albums(id)
);

-- Populate the tables
INSERT INTO bands(id,name) VALUES(1,'Seventh Wonder');
INSERT INTO bands(id,name) VALUES(2,'Metalica');
INSERT INTO bands(id,name) VALUES(3,'The Ocean');
INSERT INTO bands(id,name) VALUES(4,'Within Temptation);
INSERT INTO bands(id,name) VALUES(5,'Death');
INSERT INTO bands(id,name) VALUES(6,'Van Canto');
INSERT INTO bands(id,name) VALUES(7,'Dream Theater');

INSERT INTO albums(id,name,release_year,band_id) VALUES(1,'Tiara',2018,1);
INSERT INTO albums(id,name,release_year,band_id) VALUES(2,'The Great Escape',2010,1);
INSERT INTO albums(id,name,release_year,band_id) VALUES(3,'Mercy Falls',2008,1);
INSERT INTO albums(id,name,release_year,band_id) VALUES(4,'Master of Puppets',NULL,2);
INSERT INTO albums(id,name,release_year,band_id) VALUES(5,'...And Justice for All',1988,2);
INSERT INTO albums(id,name,release_year,band_id) VALUES(6,'Death Magnetic',2008,2);
INSERT INTO albums(id,name,release_year,band_id) VALUES(7,'Heliocentric',2010,3);
INSERT INTO albums(id,name,release_year,band_id) VALUES(8,'Pelagial',2013,3);
INSERT INTO albums(id,name,release_year,band_id) VALUES(9,'Anthropocentric',2010,3);
INSERT INTO albums(id,name,release_year,band_id) VALUES(10,'Resist',2018,4);
INSERT INTO albums(id,name,release_year,band_id) VALUES(11,'The Unforgiving',2011,4);
INSERT INTO albums(id,name,release_year,band_id) VALUES(12,'Enter',1997,4);
INSERT INTO albums(id,name,release_year,band_id) VALUES(13,'The Sound of Perservance',1998,5);
INSERT INTO albums(id,name,release_year,band_id) VALUES(14,'Individual Thought Patterns',1993,5);
INSERT INTO albums(id,name,release_year,band_id) VALUES(15,'Human',1991,5);
INSERT INTO albums(id,name,release_year,band_id) VALUES(16,'A Storm to Come',2006,6);
INSERT INTO albums(id,name,release_year,band_id) VALUES(17,'Break the Silence',2011,6);
INSERT INTO albums(id,name,release_year,band_id) VALUES(18,'Tribe of Force',2010,6);

INSERT INTO songs(id,name,length,album_id) VALUES(1,'Arrival',1+(30/60),1);
INSERT INTO songs(id,name,length,album_id) VALUES(2,'The Everones',6+(13/60),1);
INSERT INTO songs(id,name,length,album_id) VALUES(1,'Arrival',1+(30/60),1);
