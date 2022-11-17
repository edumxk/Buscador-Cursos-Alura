WHO TO USE:

need guzzle client [ "verify" => false, "base_uri"  => 'https://www.alura.com.br/'];

$url = 'cursos-online-programacao/php';

$crawler = new Crawler();

$busca = new Buscador($cliente, $crawler);

$cursos = $busca->buscar($url);

foreach($cursos as $curso) exibeMensagem($curso);
