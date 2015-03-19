---
layout:     post
title:      "Listar arquivos de pastas com PHP"
subtitle:   ""
date:       2015-02-23 00:01:00
author:     "Thiago Santos"
header-img: "img/post-bg-06.jpg"
---

<p>Olá pessoal! Veremos como listar arquivos de diretórios utilizando PHP.</p>

<p>Além de listar os arquivos, criaremos um link para o mesmo.</p>

<p>Veja o script abaixo:</p>

<pre>
<code>
<?php 
    $pasta = '../uploads/arquivos/'; 
    $diretorio = dir($pasta); 

    while ( $arquivo = $diretorio -> read() ) { 
        
        echo "<a href='".$pasta.$arquivo."'>".$arquivo."</a><br />";

    }

    $diretorio -> close();
?>
</code>
</pre>

<p>É importante que seja indicado o caminho para o diretório corretamente na variável <strong>$pasta</strong>. Logo após armazenamos o diretório absoluto na variável <strong>$diretorio</strong>.</p>
