[checkmark]: https://raw.githubusercontent.com/mozgbrasil/mozgbrasil.github.io/master/assets/images/logos/logo_32_32.png "MOZG"
![valid XHTML][checkmark]

[packagist]: https://packagist.org/packages/mozgbrasil/
[requerimentos]: http://mozgbrasil.github.io/requerimentos/
[integracao-correios]: https://github.com/mozgbrasil/magento-correios-php56#mozgcorreios
[integracao-jamef]: https://github.com/mozgbrasil/magento-jamef-php56#mozgjamef
[integracao-jadlog]: https://github.com/mozgbrasil/magento-jadlog-php56#mozgjadlog
[getcomposer]: https://getcomposer.org/
[uninstall-mods]: https://getcomposer.org/doc/03-cli.md#remove
[artigo-composer]: http://mozg.com.br/ubuntu/composer
[ioncube-loader]: http://www.ioncube.com/loaders.php
[acordo]: http://mozg.com.br/acordo-licenca-usuario-final/

# Mozg\Bundle

## Sinopse

Este é um meta pacote que instala todos os módulos da Mozg via [packagist.org][packagist] no magento

## Motivação

Atender o mercado de módulos para Magento oferecendo melhorias e um excelente suporte

## Característica técnica

Um meta-pacote é um pequeno pacote praticamente sem conteúdo algum.

A principal função deste tipo de pacote são suas dependências de outros pacotes, pois eles servem como um pacote guia para instalação específica, com suas devidas configurações.

## Instalação - Atualização - Desinstalação

--

Este módulo destina-se a ser instalado usando o [Composer][getcomposer]

Execute o seguinte comando no terminal, para visualizar a existencia do Composer e sua versão

	composer --version

Caso não tenha o Composer em seu ambiente, sugiro ler o seguinte artigo [Clique aqui][artigo-composer]

--

É necessário que o servidor tenha o suporte a extensão [ionCube PHP Loader][ioncube-loader]

Para visualizar se essa extensão está ativa em seu servidor

Certique se da presença do arquivo phpinfo.php na raiz do seu projeto

	<?php phpinfo(); ?>

Caso não exista o arquivo phpinfo.php na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

Acesse o arquivo pelo browser

Em seguida pesquise pelo termo "ionCube PHP Loader"

Caso o seu servidor não tenha o suporte a extensão, [Clique aqui][ioncube-loader]

Em "Loader Downloads API", efetue download do pacote compatível com o seu servidor

Descompacte o pacote e faça upload do arquivo "loader-wizard.php" para seu servidor, onde será demonstrado o passo a passo para a ativação da extensão

[Clique aqui](https://youtu.be/GZ2J6MLkko4) para ver os processos executados

--

Para utilizar o(s) módulo(s) da MOZG é necessário aceitar o [Acordo de licença do usuário final][acordo]

--

Sugiro manter um ambiente de testes para efeito de testes e somente após os devidos testes aplicar os devidos procedimento no ambiente de produção

--

Sugiro efetuar backup da plataforma Magento e do banco de dados

--

Antes de efetuar qualquer atualização no Magento sempre mantenha o Compiler e o Cache desativado

--

Certique se da presença do arquivo composer.json na raiz do seu projeto Magento e que o mesmo tenha os parâmetros semelhantes ao modelo JSON abaixo

	{
	  "minimum-stability": "dev",
	  "prefer-stable": true,
	  "license": [
	    "proprietary"
	  ],
	  "repositories": [
	    {
	      "type": "composer",
	      "url": "https?://packages.firegento.com"
	    }
	  ],
	  "extra": {
	    "magento-root-dir": "./",
	    "magento-deploystrategy": "copy",
	    "magento-force": true
	  }
	}

Caso não exista o arquivo composer.json na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

### Para instalar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer require mozgbrasil/magento-bundle-php56:dev-master

--

### Para atualizar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

Antes de efetuar qualquer processo que envolva atualização no Magento é recomendado manter o Compiler e Cache desativado

	composer clear-cache && composer update

Na ocorrência de erro, renomeie a pasta /vendor/mozgbrasil e execute novamente

Para checar a data do módulo execute o seguinte comando

	grep -ri --include=*.json 'time": "' ./vendor/mozgbrasil

--

### Para [desinstalar][uninstall-mods] o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer remove mozgbrasil/magento-bundle-php56 && composer clear-cache && composer update

## Perguntas mais frequentes "FAQ"

### Serviços úteis

http://www.webpagetest.org/

https://gtmetrix.com/

https://www.magereport.com/

## Contribuintes

Equipe Mozg

## Badges

[![Join the chat at https://gitter.im/mozgbrasil](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mozgbrasil/)
[![Latest Stable Version](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/v/stable)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![Total Downloads](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/downloads)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![Latest Unstable Version](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/v/unstable)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![License](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/license)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![Monthly Downloads](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/d/monthly)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![Daily Downloads](https://poser.pugx.org/mozgbrasil/magento-bundle-php56/d/daily)](https://packagist.org/packages/mozgbrasil/magento-bundle-php56)
[![Reference Status](https://www.versioneye.com/php/mozgbrasil:magento-bundle-php56/reference_badge.svg?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-bundle-php56/references)
[![Dependency Status](https://www.versioneye.com/php/mozgbrasil:magento-bundle-php56/1.0.0/badge?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-bundle-php56/1.0.0)

:cat2:
