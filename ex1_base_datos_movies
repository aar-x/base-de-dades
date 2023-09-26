-- MySQL dump 10.13  Distrib 8.0.34, for Win64 (x86_64)
--
-- Host: localhost    Database: movies
-- ------------------------------------------------------
-- Server version	8.0.34

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8mb4 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `tb_genre`
--

DROP TABLE IF EXISTS `tb_genre`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `tb_genre` (
  `genre_id` int NOT NULL,
  `genre_name` varchar(40) NOT NULL,
  `created_by_user` varchar(10) NOT NULL DEFAULT 'OS_SGAD',
  `created_date` date DEFAULT NULL,
  `updated_date` date DEFAULT NULL,
  PRIMARY KEY (`genre_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `tb_genre`
--

LOCK TABLES `tb_genre` WRITE;
/*!40000 ALTER TABLE `tb_genre` DISABLE KEYS */;
INSERT INTO `tb_genre` VALUES (1,'Acción','OS_SGAD',NULL,NULL),(2,'Ciencia Ficción','OS_SGAD',NULL,NULL),(3,'Comedia','OS_SGAD',NULL,NULL),(4,'Drama','OS_SGAD',NULL,NULL),(5,'Fantasía','apermag',NULL,NULL),(6,'Melodrama','apermag','2018-09-01','2018-09-27'),(7,'Musical','OS_SGAD',NULL,NULL),(8,'Romance','OS_SGAD',NULL,NULL),(9,'Suspense','OS_SGAD',NULL,NULL),(10,'Terror','OS_SGAD',NULL,NULL),(11,'Bélico','OS_SGAD',NULL,NULL);
/*!40000 ALTER TABLE `tb_genre` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `tb_movie`
--

DROP TABLE IF EXISTS `tb_movie`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `tb_movie` (
  `movie_id` int NOT NULL,
  `movie_title` varchar(100) NOT NULL,
  `movie_date` date DEFAULT NULL,
  `movie_format` varchar(50) DEFAULT NULL,
  `movie_genre_id` int DEFAULT NULL,
  `created_by_user` varchar(10) NOT NULL DEFAULT 'OS_SGAD',
  `created_date` date DEFAULT NULL,
  `updated_date` date DEFAULT NULL,
  PRIMARY KEY (`movie_id`),
  KEY `fk_movie_genre` (`movie_genre_id`),
  CONSTRAINT `fk_movie_genre` FOREIGN KEY (`movie_genre_id`) REFERENCES `tb_genre` (`genre_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `tb_movie`
--

LOCK TABLES `tb_movie` WRITE;
/*!40000 ALTER TABLE `tb_movie` DISABLE KEYS */;
INSERT INTO `tb_movie` VALUES (1,'Apocalypse Now','1979-05-10','Film',11,'OS_SGAD',NULL,NULL),(2,'Star Wars:Episode IV - A New Hope','1977-05-25','Film',2,'OS_SGAD',NULL,NULL),(3,'Indiana Jones and the Temple of Doom','1984-05-08','Film',1,'OS_SGAD',NULL,NULL),(4,'The Terminal','2004-06-18','Digital',3,'OS_SGAD',NULL,NULL),(5,'Jaws','1975-01-01','Film',10,'OS_SGAD',NULL,NULL),(6,'ET The Extraterrestrial','1982-07-25','Film',5,'OS_SGAD',NULL,NULL),(7,'Psycho','1960-05-06','Film',9,'OS_SGAD',NULL,NULL),(8,'Ocho Apellidos Vascos','2014-03-14','Digital',3,'OS_SGAD',NULL,NULL),(9,'Ocho Apellidos Catalanes','2016-06-09','Digital',8,'OS_SGAD',NULL,NULL),(10,'El otro lado de la cama','2002-09-04','Digital',8,'OS_SGAD',NULL,NULL),(11,'La Gran Familia Española','2012-10-15','Digital',3,'OS_SGAD',NULL,NULL),(12,'El dia de la bestia','1994-12-25','Film',1,'OS_SGAD',NULL,NULL),(13,'Braveheart','1995-08-08','Film',4,'OS_SGAD',NULL,NULL),(14,'The Shawshank Redemption','1992-01-07','Film',4,'OS_SGAD',NULL,NULL),(15,'Las brujas de Zugarramurdi','2009-10-07','Digital',9,'OS_SGAD',NULL,NULL),(16,'Blade Runner','1982-12-25','Digital',2,'OS_SGAD',NULL,NULL);
/*!40000 ALTER TABLE `tb_movie` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `tb_movie_person`
--

DROP TABLE IF EXISTS `tb_movie_person`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `tb_movie_person` (
  `movie_id` int NOT NULL,
  `person_id` int NOT NULL,
  `role_id` int NOT NULL,
  `movie_award_ind` char(1) NOT NULL,
  `created_by_user` varchar(10) NOT NULL DEFAULT 'OS_SGAD',
  `created_date` date DEFAULT NULL,
  `updated_date` date DEFAULT NULL,
  PRIMARY KEY (`movie_id`,`person_id`,`role_id`),
  KEY `fk_movper_person` (`person_id`),
  KEY `fk_movper_role` (`role_id`),
  CONSTRAINT `fk_movper_movie` FOREIGN KEY (`movie_id`) REFERENCES `tb_movie` (`movie_id`),
  CONSTRAINT `fk_movper_person` FOREIGN KEY (`person_id`) REFERENCES `tb_person` (`person_id`),
  CONSTRAINT `fk_movper_role` FOREIGN KEY (`role_id`) REFERENCES `tb_role` (`role_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `tb_movie_person`
--

LOCK TABLES `tb_movie_person` WRITE;
/*!40000 ALTER TABLE `tb_movie_person` DISABLE KEYS */;
INSERT INTO `tb_movie_person` VALUES (1,1,2,'Y','OS_SGAD',NULL,NULL),(1,1,3,'N','OS_SGAD',NULL,NULL),(1,1,5,'N','OS_SGAD',NULL,NULL),(1,2,5,'N','OS_SGAD',NULL,NULL),(1,3,1,'N','OS_SGAD',NULL,NULL),(1,4,1,'N','OS_SGAD',NULL,NULL),(1,5,1,'Y','OS_SGAD',NULL,NULL),(1,6,1,'N','OS_SGAD',NULL,NULL),(1,41,1,'N','OS_SGAD',NULL,NULL),(2,6,1,'N','OS_SGAD',NULL,NULL),(2,7,2,'Y','OS_SGAD',NULL,NULL),(2,8,3,'N','OS_SGAD',NULL,NULL),(3,6,1,'N','OS_SGAD',NULL,NULL),(3,7,1,'N','OS_SGAD',NULL,NULL),(3,7,4,'N','OS_SGAD',NULL,NULL),(3,9,2,'N','OS_SGAD',NULL,NULL),(3,10,5,'N','OS_SGAD',NULL,NULL),(4,9,2,'N','OS_SGAD',NULL,NULL),(4,9,3,'N','OS_SGAD',NULL,NULL),(4,11,1,'N','OS_SGAD',NULL,NULL),(4,12,1,'N','OS_SGAD',NULL,NULL),(5,9,2,'N','OS_SGAD',NULL,NULL),(6,9,2,'N','OS_SGAD',NULL,NULL),(7,13,1,'N','OS_SGAD',NULL,NULL),(7,13,2,'N','OS_SGAD',NULL,NULL),(7,13,3,'N','OS_SGAD',NULL,NULL),(7,14,2,'N','OS_SGAD',NULL,NULL),(7,15,2,'N','OS_SGAD',NULL,NULL),(8,16,2,'N','OS_SGAD',NULL,NULL),(8,17,1,'N','OS_SGAD',NULL,NULL),(8,18,1,'N','OS_SGAD',NULL,NULL),(8,19,1,'N','OS_SGAD',NULL,NULL),(8,20,1,'N','OS_SGAD',NULL,NULL),(9,16,2,'N','OS_SGAD',NULL,NULL),(9,17,1,'N','OS_SGAD',NULL,NULL),(9,18,1,'N','OS_SGAD',NULL,NULL),(9,19,1,'N','OS_SGAD',NULL,NULL),(9,20,1,'N','OS_SGAD',NULL,NULL),(10,16,2,'N','OS_SGAD',NULL,NULL),(11,21,2,'N','OS_SGAD',NULL,NULL),(11,21,4,'N','OS_SGAD',NULL,NULL),(11,22,1,'N','OS_SGAD',NULL,NULL),(11,23,1,'N','OS_SGAD',NULL,NULL),(11,24,1,'N','OS_SGAD',NULL,NULL),(11,25,1,'N','OS_SGAD',NULL,NULL),(11,26,1,'N','OS_SGAD',NULL,NULL),(13,28,1,'Y','OS_SGAD',NULL,NULL),(13,28,2,'N','OS_SGAD',NULL,NULL),(14,29,1,'N','OS_SGAD',NULL,NULL),(14,30,1,'N','OS_SGAD',NULL,NULL);
/*!40000 ALTER TABLE `tb_movie_person` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `tb_person`
--

DROP TABLE IF EXISTS `tb_person`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `tb_person` (
  `person_id` int NOT NULL,
  `person_name` varchar(100) NOT NULL,
  `person_country` varchar(40) DEFAULT NULL,
  `person_dob` date NOT NULL,
  `person_dod` date DEFAULT NULL,
  `person_parent_id` int DEFAULT NULL,
  `created_by_user` varchar(10) NOT NULL DEFAULT 'OS_SGAD',
  `created_date` date DEFAULT NULL,
  `updated_date` date DEFAULT NULL,
  PRIMARY KEY (`person_id`),
  KEY `fk_person_parent` (`person_parent_id`),
  CONSTRAINT `fk_person_parent` FOREIGN KEY (`person_parent_id`) REFERENCES `tb_person` (`person_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `tb_person`
--

LOCK TABLES `tb_person` WRITE;
/*!40000 ALTER TABLE `tb_person` DISABLE KEYS */;
INSERT INTO `tb_person` VALUES (1,'Francis Ford Coppola','United States','1939-04-07',NULL,NULL,'OS_SGAD',NULL,NULL),(2,'Carmine Coppola','United States','1945-07-08',NULL,NULL,'OS_SGAD',NULL,NULL),(3,'Marlon Brando','United States','1924-04-03','2004-07-01',NULL,'OS_SGAD',NULL,NULL),(4,'Robert Duvall','United States','1931-01-05',NULL,NULL,'OS_SGAD',NULL,NULL),(5,'Martin Sheen','United States','1940-08-03',NULL,NULL,'OS_SGAD',NULL,NULL),(6,'Harrison Ford','United States','1942-07-13',NULL,NULL,'OS_SGAD',NULL,NULL),(7,'George Lucas','United States','1944-05-14',NULL,NULL,'OS_SGAD',NULL,NULL),(8,'Gary Kurtz','United States','1940-07-27',NULL,NULL,'OS_SGAD',NULL,NULL),(9,'Steven Spielberg','United States','1946-12-18',NULL,NULL,'OS_SGAD',NULL,NULL),(10,'John Williams','United States','1928-08-08',NULL,NULL,'OS_SGAD',NULL,NULL),(11,'Tom Hanks','United States','1956-07-09',NULL,NULL,'OS_SGAD',NULL,NULL),(12,'Catherine Zeta-Jones','Wales','1969-09-25',NULL,NULL,'OS_SGAD',NULL,NULL),(13,'Alfred Joseph Hitchcock','United Kingdom','1899-08-13','1980-04-29',NULL,'OS_SGAD',NULL,NULL),(14,'Anthony Perkins','United States','1934-04-04','1992-09-08',NULL,'OS_SGAD',NULL,NULL),(15,'Vera Miles','United States','1929-08-23',NULL,NULL,'OS_SGAD',NULL,NULL),(16,'Emilio Martinez Lazaro','Spain','1956-09-09',NULL,NULL,'OS_SGAD',NULL,NULL),(17,'Dani Rovira','Spain','1984-07-01',NULL,NULL,'OS_SGAD',NULL,NULL),(18,'Clara Lago','Spain','1986-04-17',NULL,NULL,'OS_SGAD',NULL,NULL),(19,'Carmen Machi','Spain','1964-08-09',NULL,NULL,'OS_SGAD',NULL,NULL),(20,'Karra Elejalde','Spain','1960-03-06',NULL,NULL,'OS_SGAD',NULL,NULL),(21,'Daniel Sanchez Arevalo','Spain','1970-06-08',NULL,NULL,'OS_SGAD',NULL,NULL),(22,'Quim Gutierrez','Spain','1981-03-27',NULL,NULL,'OS_SGAD',NULL,NULL),(23,'Robert Alamo','Spain','1970-05-06',NULL,NULL,'OS_SGAD',NULL,NULL),(24,'Hector Colome','Spain','1944-10-25','2015-02-28',NULL,'OS_SGAD',NULL,NULL),(25,'Veronica Echegui','Spain','1983-03-14',NULL,NULL,'OS_SGAD',NULL,NULL),(26,'Patrick Criado','Spain','1995-09-23',NULL,NULL,'OS_SGAD',NULL,NULL),(27,'Sean Connery','Scotland','1930-07-08',NULL,NULL,'OS_SGAD',NULL,NULL),(28,'Mel Gibson','Australia','1950-08-09',NULL,NULL,'OS_SGAD',NULL,NULL),(29,'Morgan Freeman','United States','1935-10-01',NULL,NULL,'OS_SGAD',NULL,NULL),(30,'Tim Robbins','United States','1949-06-07',NULL,NULL,'OS_SGAD',NULL,NULL),(41,'Charlie Sheen','United States','1965-09-03',NULL,5,'OS_SGAD',NULL,NULL),(42,'Emilio Estevez','United States','1962-05-12',NULL,5,'OS_SGAD',NULL,NULL),(43,'Ramón Estevez','United States','1963-08-07',NULL,5,'OS_SGAD',NULL,NULL),(44,'Reneé Estevez','United States','1967-04-02',NULL,5,'OS_SGAD',NULL,NULL),(45,'Paula Speert Sheen','United States','1986-01-06',NULL,41,'OS_SGAD',NULL,NULL),(46,'Bob Sheen','United States','2009-05-01',NULL,41,'OS_SGAD',NULL,NULL),(47,'Max Sheen','United States','2009-05-01',NULL,41,'OS_SGAD',NULL,NULL),(48,'Sam Sheen','United States','2004-03-09',NULL,41,'OS_SGAD',NULL,NULL),(49,'Lola Sheen','United States','2005-06-01',NULL,41,'OS_SGAD',NULL,NULL),(50,'Paula Jones-Sheen','United States','2003-07-06',NULL,45,'OS_SGAD',NULL,NULL),(51,'Paloma Rae Estevez','United States','1986-02-15',NULL,42,'OS_SGAD',NULL,NULL),(52,'Taylor Levi Estevez','United States','1984-06-22',NULL,42,'OS_SGAD',NULL,NULL);
/*!40000 ALTER TABLE `tb_person` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `tb_role`
--

DROP TABLE IF EXISTS `tb_role`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `tb_role` (
  `role_id` int NOT NULL,
  `role_name` varchar(60) NOT NULL,
  `created_by_user` varchar(10) NOT NULL DEFAULT 'OS_SGAD',
  `created_date` date DEFAULT NULL,
  `updated_date` date DEFAULT NULL,
  PRIMARY KEY (`role_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `tb_role`
--

LOCK TABLES `tb_role` WRITE;
/*!40000 ALTER TABLE `tb_role` DISABLE KEYS */;
INSERT INTO `tb_role` VALUES (1,'Actor','OS_SGAD',NULL,NULL),(2,'Director','OS_SGAD',NULL,NULL),(3,'Productor','OS_SGAD',NULL,NULL),(4,'Guionista','OS_SGAD',NULL,NULL),(5,'Música','OS_SGAD',NULL,NULL);
/*!40000 ALTER TABLE `tb_role` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2023-09-22 11:35:18
