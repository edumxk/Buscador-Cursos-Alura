WHO TO USE:

<?php

require __DIR__ . '/vendor/autoload.php';

use Edumxk\BuscadorDeCursos\Buscador;
use GuzzleHttp\Client;
use Symfony\Component\DomCrawler\Crawler;


$cliente = new client([ "verify" => false, "base_uri"  => 'https://www.alura.com.br/']);

$url = 'cursos-online-programacao/php';

$crawler = new Crawler();

$busca = new Buscador($cliente, $crawler);

$cursos = $busca->buscar($url);

foreach($cursos as $curso) exibeMensagem($curso);
