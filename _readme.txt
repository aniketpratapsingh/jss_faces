

To get you going:

1) upload all files to your website/testspace or whereever you wanna play with it.
2) setup your database - look in the file: mysql.php
3) execute this SQL to setup your database tables:

		CREATE TABLE IF NOT EXISTS `battles` (
			`battle_id` bigint(20) unsigned NOT NULL auto_increment,
			`winner` bigint(20) unsigned NOT NULL,
			`loser` bigint(20) unsigned NOT NULL,
			PRIMARY KEY  (`battle_id`),
			KEY `winner` (`winner`)
		) ENGINE=MyISAM  DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;
		
		
		CREATE TABLE IF NOT EXISTS `images` (
			`image_id` bigint(20) unsigned NOT NULL auto_increment,
			`filename` varchar(255) NOT NULL,
			`score` int(10) unsigned NOT NULL default '1500',
			`wins` int(10) unsigned NOT NULL default '0',
			`losses` int(10) unsigned NOT NULL default '0',
			PRIMARY KEY  (`image_id`)
		) ENGINE=MyISAM  DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;

4) place all your images that's up for battle in the /imagees/ folder.
5) run the /install_images.php from your site to install all images from your folder into your database.
6) have fun!









