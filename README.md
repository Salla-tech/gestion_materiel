# gestion_materiel
Une application développer en php 7 avec bootstrap twitter pour faire la gestion des matériel d'un studio. C'est à dire gérer les entrées et sortie des différents matériel sortie par le personnel.
La base de données s'appel saharamedia
l'identifiant et le mot de passe sont root et le mot de passe est vide.
Fichier configuration base de données Class/App.php
<?php

/**
 * Created by PhpStorm.
 * User: Souhaibou
 * Date: 12/01/2019
 * Time: 11:17
 */
class App{
	static $db = null;
	static function getDatabase(){

		if (!self::$db) {
			self:: $db = new Database('root','','saharamedia');
		}
		
		return self::$db;
	}

	static function redirect($page){
		header("location: $page");
		exit();
	}
}
L'application est ddévelopper en orientée objet.
Pour d'autres information de configuration envoyer un message a souhaibou04@gmail.com
