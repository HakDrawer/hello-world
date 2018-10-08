# hello-world
тест$xhe_host ="127.0.0.1:7010";
 
// The following code is required to properly run XWeb Human Emulator
require("../Templates/xweb_human_emulator.php");
 
// переходим на страницу google.com
$browser->navigate("http://www.google.com");
// wait on browser
$browser->wait_for(30,1);
 
// задаём в поле поиска x-scripts.com
$input->set_value_by_name('q','x-scripts.com');
// нажимаем кнопку искать
$button->click_by_name('btnK');
// ждём пока браузер загрузит страницу
$browser->wait_for(30,1);
 
// кликнем по ссылке с текстом x-scripts.com
$anchor->click_by_inner_text('x-scripts.com',false);
// ждём пока браузер загрузит страницу
$browser->wait_for(30,1);
 
// Quit
$app->quit();

