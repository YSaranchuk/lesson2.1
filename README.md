<?php
	$jsonData = file_get_contents('phones.json');
	$data = json_decode($jsonData);
?>
<!DOCTYPE html>
<html lang="ru">
<head>
	<meta charset="UTF-8">
	<link rel="stylesheet" type="text/css" href="style.css">
	<title>Установка и настройка веб-сервера.</title>
</head>
<body>
	<table>
		<tr>
			<th>Имя</th>
			<th>Фамилия</th>
			<th>Адрес</th>
			<th>Телефон</th>
		</tr>
		<?php foreach ($data as $card) {?>
		<tr>
			<td><?=$card->firstName;?></td>
			<td><?=$card->lastName;?></td>
			<td><?=$card->address;?></td>
			<td><?=$card->phoneNumber;?></td>
		</tr>
		<?php } ?>
	</table>
</body>
</html>
