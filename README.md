# BDD_Luya_CHarbonnier

# Projet Logement_BDD

Le but du projet est de comprendre et faire fonctionner une Base de Données à multitable

---

## Table des matières

- [À propos](#à-propos)
- [Fonctionnalités](#fonctionnalités)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Contribuer](#contribuer)
- [Licence](#licence)

---

## À propos

Le but de se projet est d'apprendre à créer et administrer une Base de Données à plusieurs tables.
Ce projet a été développé dans le cadre d'un projet d'études en BTS CIEL spécialité IR.

## Fonctionnalités

- Définir une base de données de vendeur et d'acheteur de propriétés, avec les logements vendues et les employés qui s'occupe de cette vente.

## Installation
La BDD est importable soit depuis le lien ci-dessous, soit avec le texte raw a impémenter dans la partie IMPORT dans phpmyadmin.



[Uplo-- phpMyAdmin SQL Dump
-- version 5.2.1
-- https://www.phpmyadmin.net/
--
-- Host: mysql-charbobo.alwaysdata.net
-- Generation Time: Nov 12, 2024 at 08:18 AM
-- Server version: 10.11.8-MariaDB
-- PHP Version: 7.4.33

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `charbobo_projet3`
--

-- --------------------------------------------------------

--
-- Table structure for table `Acheteur`
--

CREATE TABLE `Acheteur` (
  `id_acheteur` int(11) NOT NULL,
  `Nom` varchar(45) DEFAULT NULL,
  `Prénom` varchar(45) DEFAULT NULL,
  `Tel` int(10) DEFAULT NULL,
  `Mail` varchar(45) DEFAULT NULL,
  `Budget` varchar(50) DEFAULT NULL,
  `id_employé` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `Acheteur`
--

INSERT INTO `Acheteur` (`id_acheteur`, `Nom`, `Prénom`, `Tel`, `Mail`, `Budget`, `id_employé`) VALUES
(1, 'Nold', 'Leo', 1102030405, 'leonold@exemple.fr', '150000', 1),
(25, 'Carroll', 'Ruby', 7, 'dolor.dolor.tempus@hotmail.org', '625410', 1),
(26, 'Hughes', 'Halla', 6, 'nec.cursus@google.couk', '325361', 1),
(27, 'O\'brien', 'Rebecca', 6, 'nec.tempus@outlook.edu', '199527', 1),
(28, 'Moody', 'Portia', 4, 'lobortis.augue@icloud.com', '13321', 1),
(29, 'Herring', 'Igor', 5, 'sollicitudin.adipiscing.ligula@outlook.org', '289861', 1),
(30, 'Leblanc', 'Trevor', 3, 'elit.nulla@yahoo.com', '587888', 1),
(31, 'Dunlap', 'Inga', 4, 'nascetur.ridiculus@google.org', '318175', 1),
(32, 'Miles', 'Elvis', 6, 'et@yahoo.ca', '394741', 1),
(33, 'Hoffman', 'Phillip', 6, 'velit.sed@outlook.com', '952356', 1),
(34, 'Pate', 'Amos', 6, 'mauris.sagittis@yahoo.couk', '733112', 1),
(35, 'Clements', 'Noah', 7, 'quisque.fringilla@icloud.ca', '420461', 1),
(36, 'Mcguire', 'Audrey', 3, 'ipsum.dolor@google.ca', '381125', 1),
(37, 'Norris', 'Claudia', 5, 'consectetuer@google.edu', '497030', 1),
(38, 'Nolan', 'David', 3, 'sed.pharetra@icloud.net', '924464', 1),
(39, 'Gamble', 'Iris', 7, 'convallis.erat.eget@outlook.couk', '830044', 1),
(40, 'O\'brien', 'Buckminster', 7, 'sed.dolor.fusce@yahoo.ca', '32486', 1),
(41, 'Little', 'Berk', 6, 'dolor@yahoo.com', '802963', 1),
(42, 'Navarro', 'Gray', 4, 'orci@hotmail.org', '965597', 1),
(43, 'Bender', 'Madaline', 5, 'tellus.justo@icloud.edu', '684926', 1),
(44, 'Rivas', 'Irene', 8, 'mauris@protonmail.com', '502341', 1),
(45, 'Mills', 'Axel', 7, 'nonummy@outlook.com', '537983', 1),
(46, 'Craft', 'Kato', 8, 'orci@yahoo.net', '768439', 1),
(47, 'Bray', 'Camille', 6, 'erat.sed@icloud.edu', '784744', 1),
(48, 'Santana', 'Dale', 3, 'hendrerit.neque.in@protonmail.couk', '946572', 1),
(49, 'Rasmussen', 'Jescie', 7, 'nulla@outlook.net', '320527', 1),
(50, 'Floyd', 'Abbot', 6, 'nulla.vulputate@protonmail.com', '814851', 1),
(51, 'Erickson', 'Abraham', 4, 'libero.morbi@outlook.couk', '993321', 1),
(52, 'Bridges', 'Deacon', 2, 'non.sapien@aol.net', '537555', 1),
(53, 'Carey', 'Tarik', 4, 'eu@protonmail.edu', '516988', 1),
(54, 'Le', 'Kirk', 4, 'nullam.feugiat.placerat@icloud.edu', '540050', 1),
(55, 'Gibbs', 'Nyssa', 6, 'etiam.ligula@icloud.couk', '173347', 1),
(56, 'Orr', 'Eagan', 3, 'purus.duis.elementum@protonmail.org', '124148', 1),
(57, 'Frank', 'Odysseus', 9, 'a@hotmail.edu', '713563', 1),
(58, 'Mcintosh', 'Barclay', 1, 'vel@yahoo.ca', '798852', 1),
(59, 'Gardner', 'Rama', 9, 'tincidunt@outlook.org', '595131', 1),
(60, 'Silva', 'Keith', 6, 'libero.et@google.edu', '138618', 1),
(61, 'Small', 'Ulla', 5, 'commodo.ipsum@outlook.com', '770470', 1),
(62, 'Mccoy', 'Shaeleigh', 7, 'eu.placerat@google.com', '800388', 1),
(63, 'Kim', 'Yoshi', 2, 'et.eros@aol.couk', '763089', 1),
(64, 'Gay', 'Ramona', 4, 'et.magnis@google.com', '175002', 1),
(65, 'Malone', 'Leroy', 6, 'purus.maecenas.libero@yahoo.couk', '238235', 1),
(66, 'Hess', 'Halla', 7, 'purus@outlook.couk', '223574', 1),
(67, 'Fields', 'Magee', 8, 'nec.tempus.mauris@protonmail.ca', '480015', 1),
(68, 'Schultz', 'Sara', 8, 'sem@protonmail.net', '757295', 1),
(69, 'Wilkinson', 'Farrah', 8, 'donec.est.nunc@yahoo.edu', '619500', 1),
(70, 'Whitfield', 'Deirdre', 2, 'eget@google.couk', '32176', 1),
(71, 'Burch', 'Aline', 8, 'nunc.commodo@icloud.org', '12989', 1),
(72, 'Small', 'Paki', 1, 'accumsan.sed@aol.couk', '350122', 1),
(73, 'Graham', 'Nerea', 8, 'nunc@protonmail.org', '303168', 1),
(74, 'Short', 'Brady', 2, 'suspendisse.aliquet@hotmail.org', '888191', 1),
(75, 'Valenzuela', 'Ella', 2, 'ullamcorper.duis.cursus@hotmail.edu', '918652', 1),
(76, 'Robinson', 'Virginia', 8, 'ornare.sagittis@aol.net', '43372', 1),
(77, 'Wilkinson', 'Leigh', 6, 'aliquam@hotmail.ca', '469536', 1),
(78, 'Kirk', 'Zorita', 7, 'eget.metus@yahoo.com', '752364', 1),
(79, 'Franks', 'Sonya', 3, 'in.lorem@protonmail.com', '249110', 1),
(80, 'Bradford', 'Ingrid', 9, 'sed.tortor@aol.org', '173253', 1),
(81, 'Noel', 'Quemby', 6, 'amet.ornare@outlook.couk', '589456', 1),
(82, 'Kelley', 'Rashad', 6, 'scelerisque.neque.sed@google.couk', '248470', 1),
(83, 'Juarez', 'Susan', 4, 'aliquam@google.com', '458635', 1),
(84, 'Vega', 'Xavier', 3, 'fermentum.convallis.ligula@aol.ca', '631403', 1),
(85, 'Sosa', 'Louis', 9, 'tincidunt.donec@outlook.ca', '495509', 1),
(86, 'Huff', 'Vielka', 5, 'curabitur@yahoo.net', '779955', 1),
(87, 'Mcleod', 'Freya', 7, 'tempor@icloud.couk', '117506', 1),
(88, 'Rowland', 'Slade', 3, 'eu.nibh.vulputate@hotmail.couk', '417775', 1),
(89, 'Finch', 'Boris', 8, 'arcu.morbi@protonmail.couk', '975527', 1),
(90, 'Adams', 'Kareem', 7, 'cras.sed.leo@hotmail.com', '864928', 1),
(91, 'Mcdowell', 'Graiden', 7, 'ante.dictum@protonmail.com', '568899', 1),
(92, 'Ingram', 'Xanthus', 6, 'fames@aol.ca', '442414', 1),
(93, 'Butler', 'Marshall', 3, 'imperdiet@yahoo.ca', '649689', 1),
(94, 'Harper', 'Alec', 3, 'lobortis.tellus.justo@icloud.org', '28286', 1),
(95, 'Montoya', 'Carter', 4, 'curabitur.sed@yahoo.org', '933263', 1),
(96, 'Berger', 'Kenneth', 8, 'nulla.facilisi@hotmail.org', '412921', 1),
(97, 'Pena', 'Rahim', 8, 'arcu.ac@aol.edu', '193962', 1),
(98, 'Spears', 'Xena', 6, 'ante@hotmail.ca', '281731', 1),
(99, 'Case', 'Kelly', 3, 'varius.et@protonmail.ca', '739159', 1),
(100, 'Webb', 'Vernon', 5, 'vitae.erat.vivamus@protonmail.couk', '568485', 1),
(101, 'Rios', 'Paloma', 2, 'phasellus.libero@protonmail.net', '181831', 1),
(102, 'Ferrell', 'Sybil', 9, 'quam.a.felis@hotmail.ca', '800415', 1),
(103, 'Velasquez', 'Beau', 8, 'in@outlook.ca', '622072', 1),
(104, 'Flowers', 'Xandra', 5, 'sed.pharetra.felis@aol.net', '434977', 1),
(105, 'Terry', 'Daryl', 5, 'ut.aliquam.iaculis@google.org', '835668', 1),
(106, 'Ray', 'Kennan', 4, 'proin.vel.nisl@protonmail.net', '713951', 1),
(107, 'Moon', 'Harlan', 3, 'non.lorem.vitae@hotmail.couk', '244051', 1),
(108, 'O\'Neill', 'Tate', 7, 'pede.cum@outlook.edu', '186391', 1),
(109, 'Greene', 'Aquila', 3, 'dui.nec.urna@icloud.net', '602105', 1),
(110, 'Bradley', 'Calvin', 9, 'tempus@icloud.edu', '177701', 1),
(111, 'Tucker', 'Orson', 7, 'urna.et.arcu@yahoo.com', '544842', 1),
(112, 'Riley', 'Oliver', 3, 'etiam@aol.couk', '278155', 1),
(113, 'Garza', 'Dante', 7, 'cras.eget@yahoo.edu', '401547', 1),
(114, 'Douglas', 'Giacomo', 5, 'massa.suspendisse@outlook.org', '608014', 1),
(115, 'Cameron', 'Quinlan', 8, 'volutpat.nulla@yahoo.org', '107661', 1),
(116, 'Mason', 'Morgan', 5, 'imperdiet.ullamcorper.duis@protonmail.net', '448158', 1),
(117, 'Stuart', 'Elliott', 2, 'aliquam.nisl@yahoo.org', '34567', 1),
(118, 'Miranda', 'Winter', 9, 'luctus.ipsum@protonmail.couk', '247741', 1),
(119, 'Cote', 'Tarik', 4, 'nibh.donec.est@aol.edu', '250902', 1),
(120, 'Fuller', 'Hayes', 2, 'lorem.auctor@outlook.net', '849501', 1),
(121, 'Pope', 'Wayne', 1, 'enim.consequat@icloud.ca', '573317', 1),
(122, 'Reeves', 'Lael', 6, 'venenatis.vel@aol.net', '689768', 1),
(123, 'Knowles', 'Leroy', 4, 'diam.vel@outlook.net', '79158', 1),
(124, 'Cline', 'Maya', 2, 'dui@google.com', '350546', 1);

-- --------------------------------------------------------

--
-- Table structure for table `Employé`
--

CREATE TABLE `Employé` (
  `id_employé` int(11) NOT NULL,
  `Nom` varchar(45) DEFAULT NULL,
  `Prénom` varchar(45) DEFAULT NULL,
  `id_logement` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `Employé`
--

INSERT INTO `Employé` (`id_employé`, `Nom`, `Prénom`, `id_logement`) VALUES
(1, 'Negrel', 'Thomas', 1),
(3, 'Phillips', 'Kim', 49),
(4, 'Austin', 'Elijah', 40),
(5, 'Mcneil', 'Amos', 46),
(6, 'Blackburn', 'Yeo', 50),
(7, 'Cherry', 'Harriet', 44),
(8, 'Park', 'Selma', 7),
(9, 'Greene', 'Benedict', 11),
(10, 'Leblanc', 'Flynn', 13),
(11, 'Bray', 'Hunter', 50),
(12, 'Dawson', 'Lana', 35),
(13, 'Pratt', 'Jana', 15),
(14, 'Shields', 'Blossom', 23),
(15, 'Dawson', 'Jackson', 12);

-- --------------------------------------------------------

--
-- Table structure for table `Logement`
--

CREATE TABLE `Logement` (
  `id_logement` int(11) NOT NULL,
  `Adresse` varchar(45) DEFAULT NULL,
  `Ville` varchar(45) DEFAULT NULL,
  `Prix` int(11) DEFAULT NULL,
  `id_vendeur` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `Logement`
--

INSERT INTO `Logement` (`id_logement`, `Adresse`, `Ville`, `Prix`, `id_vendeur`) VALUES
(1, '123 Rue de Paris', 'Paris', 500000, 1),
(2, 'P.O. Box 210, 8115 Mi Avenue', 'Burnie', 949455, 28),
(3, '8537 Dictum St.', 'Arviat', 977203, 13),
(4, 'Ap #729-1076 Congue, St.', 'Cessnock', 94216, 12),
(5, 'Ap #986-7123 Elit, Street', 'Utrecht', 82222, 45),
(6, 'P.O. Box 945, 8940 Dictum Av.', 'Llanelli', 203599, 37),
(7, 'Ap #115-4957 Iaculis St.', 'Osnabrück', 726269, 30),
(8, 'P.O. Box 193, 2942 Lorem Avenue', 'Yên Ninh', 109012, 24),
(9, '176-6163 Lectus Ave', 'Ceuta', 919360, 46),
(10, 'Ap #858-1608 Mus. Road', 'Moscow', 511962, 37),
(11, 'P.O. Box 787, 8131 Non, St.', 'Trà Vinh', 898582, 10),
(12, 'Ap #248-2531 Morbi Rd.', 'Flekkefjord', 940380, 16),
(13, '9461 In Avenue', 'Puno', 940848, 11),
(14, '733-4989 Pretium Street', 'Girardot', 833676, 25),
(15, 'Ap #483-2740 Nec Street', 'Dnipro', 590996, 14),
(16, 'Ap #856-412 Luctus Avenue', 'Motala', 425505, 23),
(17, 'P.O. Box 841, 8027 Convallis Rd.', 'Adana', 692387, 26),
(18, 'Ap #537-5798 Neque Rd.', 'Kursk', 233126, 44),
(19, 'P.O. Box 620, 1180 Metus Road', 'Pessac', 628754, 33),
(20, '639-6091 Pellentesque Ave', 'Shimla', 341449, 40),
(21, 'P.O. Box 678, 9887 Integer St.', 'Saratov', 326819, 50),
(22, 'Ap #247-4491 Pellentesque Avenue', 'Málaga', 881213, 40),
(23, 'Ap #366-2197 Odio St.', 'Kapfenberg', 108431, 27),
(24, '746-148 Pede, Road', 'Kaneohe', 929318, 32),
(25, 'P.O. Box 631, 5103 Eu, St.', 'Nivelles', 522724, 40),
(26, '165-2930 Sociis Rd.', 'Ceuta', 546450, 10),
(27, 'P.O. Box 168, 228 Ipsum. St.', 'Wick', 455838, 18),
(28, '203-6503 Urna Street', 'Bagh', 385328, 47),
(29, '390-1306 Velit. Av.', 'Medan', 88214, 26),
(30, 'Ap #749-3636 Lobortis Rd.', 'Ereğli', 946058, 3),
(31, 'Ap #141-1823 Lorem, Street', 'Canberra', 524905, 51),
(32, '648-3345 At Rd.', 'Lelystad', 724990, 47),
(33, 'Ap #136-4719 Torquent Av.', 'Jecheon', 137997, 46),
(34, 'Ap #518-1631 Fusce Rd.', 'Kadiyivka', 36010, 10),
(35, 'Ap #121-736 Nibh. Street', 'Petrolina', 426143, 44),
(36, 'P.O. Box 431, 8366 A, Avenue', 'Serangoon', 580964, 34),
(37, '1873 Rutrum, Rd.', 'Hastings', 663821, 47),
(38, 'Ap #124-1716 Et, Avenue', 'Pugwash', 667558, 46),
(39, '761-2414 Malesuada. St.', 'Vottem', 375676, 14),
(40, '412-3625 Mus. Av.', 'Quezon City', 904031, 14),
(41, 'Ap #786-7012 Fermentum Av.', 'Vienna', 346689, 49),
(42, '150-5679 Cras Rd.', 'Patarrá', 51954, 8),
(43, '5090 Aliquam Avenue', 'Juárez', 106888, 38),
(44, 'Ap #726-4505 Sem St.', 'Vallenar', 698132, 19),
(45, 'Ap #713-1055 Porttitor Ave', 'Oaxaca', 182724, 6),
(46, '427-9218 Sagittis Rd.', 'Orito', 376148, 35),
(47, 'Ap #176-1657 Lobortis Road', 'Bergen', 42072, 9),
(48, 'P.O. Box 850, 6007 Diam. Street', 'Mata de Plátano', 933016, 45),
(49, 'Ap #102-9811 Nonummy Rd.', 'Kielce', 770597, 22),
(50, 'Ap #745-9944 Ullamcorper Street', 'Lede', 958719, 14),
(51, 'P.O. Box 899, 2873 Purus. St.', 'Mustafakemalpaşa', 97434, 7);

-- --------------------------------------------------------

--
-- Table structure for table `Vendeur`
--

CREATE TABLE `Vendeur` (
  `id_vendeur` int(11) NOT NULL,
  `Nom` varchar(45) DEFAULT NULL,
  `Prénom` varchar(45) DEFAULT NULL,
  `Tel` int(11) DEFAULT NULL,
  `Mail` varchar(45) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `Vendeur`
--

INSERT INTO `Vendeur` (`id_vendeur`, `Nom`, `Prénom`, `Tel`, `Mail`) VALUES
(1, 'Dupont', 'Jean', 123456789, 'jean.dupont@example.com'),
(2, 'Robertson', 'Seth', 2, 'varius@icloud.ca'),
(3, 'Wilkinson', 'Salvador', 2, 'a.scelerisque.sed@yahoo.edu'),
(4, 'Madden', 'Ali', 2, 'at@outlook.net'),
(5, 'Cortez', 'Amir', 9, 'gravida.nunc.sed@aol.edu'),
(6, 'Pollard', 'Mallory', 7, 'ut.eros.non@icloud.ca'),
(7, 'Moody', 'Colin', 6, 'mauris.aliquam@google.com'),
(8, 'Burke', 'Marsden', 4, 'id.libero.donec@google.ca'),
(9, 'Bullock', 'Kitra', 4, 'adipiscing.lacus@hotmail.com'),
(10, 'Donovan', 'Doris', 5, 'lacus.quisque@icloud.edu'),
(11, 'Rios', 'Jade', 1, 'varius.et.euismod@hotmail.net'),
(12, 'Pickett', 'Dominique', 4, 'elit.erat.vitae@outlook.ca'),
(13, 'Abbott', 'Maggy', 6, 'aliquet@icloud.ca'),
(14, 'Byrd', 'Ulysses', 6, 'ante.lectus.convallis@outlook.net'),
(15, 'Kline', 'Mary', 6, 'sed.turpis@protonmail.org'),
(16, 'Bean', 'Philip', 7, 'auctor.velit@icloud.edu'),
(17, 'Burgess', 'Hayfa', 3, 'vel.mauris.integer@yahoo.edu'),
(18, 'Key', 'Cole', 9, 'suspendisse.tristique.neque@yahoo.net'),
(19, 'Rivera', 'Suki', 9, 'praesent@hotmail.net'),
(20, 'Hewitt', 'Boris', 5, 'elit.etiam.laoreet@hotmail.com'),
(21, 'Stark', 'Riley', 4, 'in@google.net'),
(22, 'Walter', 'Serina', 8, 'id@outlook.ca'),
(23, 'Hammond', 'Madeson', 8, 'suspendisse@protonmail.com'),
(24, 'Moran', 'Whitney', 4, 'quam.quis.diam@protonmail.org'),
(25, 'Shaffer', 'Robert', 1, 'magna.cras.convallis@yahoo.couk'),
(26, 'Nixon', 'Eagan', 2, 'eget@outlook.couk'),
(27, 'Trevino', 'Kathleen', 5, 'nam@hotmail.org'),
(28, 'Harris', 'Lareina', 4, 'pede.ultrices.a@icloud.ca'),
(29, 'Hardy', 'Rashad', 2, 'aliquet.lobortis.nisi@outlook.ca'),
(30, 'Juarez', 'Honorato', 7, 'ipsum.primis@hotmail.com'),
(31, 'Meyers', 'Hayes', 6, 'vitae.posuere@yahoo.edu'),
(32, 'Madden', 'Oren', 5, 'elementum.sem.vitae@yahoo.couk'),
(33, 'Glass', 'Brock', 5, 'ac.feugiat@google.org'),
(34, 'Mendoza', 'Malachi', 9, 'erat.neque.non@outlook.net'),
(35, 'Conway', 'Ahmed', 6, 'eget.massa@aol.edu'),
(36, 'Mclean', 'Nathan', 7, 'lobortis.ultrices@google.couk'),
(37, 'Mays', 'Sandra', 6, 'nulla.magna@protonmail.edu'),
(38, 'Mckinney', 'Ralph', 7, 'pede.nec.ante@icloud.com'),
(39, 'Duke', 'Gareth', 4, 'senectus.et.netus@google.com'),
(40, 'Humphrey', 'Dominic', 5, 'tristique.ac@outlook.couk'),
(41, 'Barker', 'Lenore', 7, 'accumsan@protonmail.edu'),
(42, 'Pennington', 'Zeus', 9, 'lorem.sit@google.edu'),
(43, 'Daugherty', 'Francesca', 2, 'cras.dictum@yahoo.edu'),
(44, 'Ross', 'Drew', 4, 'cras.sed@protonmail.couk'),
(45, 'Stein', 'Alvin', 9, 'diam.luctus@icloud.ca'),
(46, 'Shaw', 'Abraham', 9, 'euismod.in@protonmail.ca'),
(47, 'Harvey', 'Veronica', 9, 'faucibus@icloud.net'),
(48, 'Villarreal', 'Summer', 6, 'pede.praesent@outlook.ca'),
(49, 'Cotton', 'Jin', 2, 'sit.amet@outlook.net'),
(50, 'O\'donnell', 'Raphael', 6, 'sed.sapien.nunc@outlook.com'),
(51, 'Travis', 'Carolyn', 7, 'lorem.donec@outlook.ca');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `Acheteur`
--
ALTER TABLE `Acheteur`
  ADD PRIMARY KEY (`id_acheteur`),
  ADD KEY `fk_Client_employé1_idx` (`id_employé`);

--
-- Indexes for table `Employé`
--
ALTER TABLE `Employé`
  ADD PRIMARY KEY (`id_employé`),
  ADD KEY `fk_employé_maison1_idx` (`id_logement`);

--
-- Indexes for table `Logement`
--
ALTER TABLE `Logement`
  ADD PRIMARY KEY (`id_logement`),
  ADD KEY `fk_maison_vendeur_idx` (`id_vendeur`);

--
-- Indexes for table `Vendeur`
--
ALTER TABLE `Vendeur`
  ADD PRIMARY KEY (`id_vendeur`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `Acheteur`
--
ALTER TABLE `Acheteur`
  MODIFY `id_acheteur` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=125;

--
-- AUTO_INCREMENT for table `Employé`
--
ALTER TABLE `Employé`
  MODIFY `id_employé` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=16;

--
-- AUTO_INCREMENT for table `Logement`
--
ALTER TABLE `Logement`
  MODIFY `id_logement` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=52;

--
-- AUTO_INCREMENT for table `Vendeur`
--
ALTER TABLE `Vendeur`
  MODIFY `id_vendeur` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=52;

--
-- Constraints for dumped tables
--

--
-- Constraints for table `Acheteur`
--
ALTER TABLE `Acheteur`
  ADD CONSTRAINT `fk_Client_employé1` FOREIGN KEY (`id_employé`) REFERENCES `Employé` (`id_employé`) ON DELETE NO ACTION ON UPDATE NO ACTION;

--
-- Constraints for table `Employé`
--
ALTER TABLE `Employé`
  ADD CONSTRAINT `fk_employé_maison1` FOREIGN KEY (`id_logement`) REFERENCES `Logement` (`id_logement`) ON DELETE NO ACTION ON UPDATE NO ACTION;

--
-- Constraints for table `Logement`
--
ALTER TABLE `Logement`
  ADD CONSTRAINT `fk_maison_vendeur` FOREIGN KEY (`id_vendeur`) REFERENCES `Vendeur` (`id_vendeur`) ON DELETE NO ACTION ON UPDATE NO ACTION;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;

