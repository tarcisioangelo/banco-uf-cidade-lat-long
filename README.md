# banco-uf-cidade-lat-long

Banco de dados com cidades e ufs do Brasil com Latitude e Longitude


CREATE TABLE IF NOT EXISTS `tb_cidade` (
  `idCidade` int(11) NOT NULL AUTO_INCREMENT,
  `idUF` int(11) NOT NULL,
  `dsCidade` varchar(70) NOT NULL,
  `latitude` varchar(45) DEFAULT NULL,
  `longitude` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`idCidade`),
  KEY `fk_tb_cidade_tb_uf1_idx` (`idUF`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=6095 ;



CREATE TABLE IF NOT EXISTS `tb_uf` (
  `idUF` int(11) NOT NULL AUTO_INCREMENT,
  `sgUF` varchar(2) NOT NULL,
  `dsUF` varchar(45) NOT NULL,
  `latitude` varchar(45) DEFAULT NULL,
  `longitude` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`idUF`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=28 ;


