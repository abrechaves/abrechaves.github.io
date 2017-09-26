---
layout: post
title: "Design smells"
date: 2016-07-14 14:11:24 -0300
comments: true
author: Gesiel Silva
categories: [Clean code, design smells, refactoring, SOLID]
published: true 
---
<p align="justify">
    Como desenvolvedor, foram inúmeras as vezes que me deparei com <em>design smells</em>. O problema é que muitos desenvolvedores não sabem o que estão fazendo de errado e nem quais consequências terão mediante suas decisões. Precisamos dar nomes a esses problemas e ter argumentos que dão embasamento à escolha de boas práticas de desenvolvimento. Mas afinal, quais são os principais mau cheiros no desenvolvimento de software?
</p>
<!-- more -->
<p align="justify">
	São quatro os <em>design smells</em> que vou tratar nesse post: Rigidez, Fragilidade, Imobilidade e Viscosidade.
	<strong>Rigidez</strong> é quando o custo de uma alteração no software é muito alto do ponto de vista de build. Ou seja, quando o tempo de build e de execução da sua suíte de testes é elevado demais, provavelmente temos um problema de rigidez. Temos que nos concientizar que um ambiente ideal de desenvolvimento deve dar feedbacks frequentes ao desenvolvedor, e por tanto, os testes devem executar o mais rápido possível, preferencialmente em poucos segundos. Além disso, builds demorados podem onerar o desempenho da IDE utilizada para desenvolvimento.
</p>
<p align="justify">
	<strong>Fragilidade</strong> é quando alterações em um determinado módulo da aplicação acaba por ocasionar erros e/ou situações inesperadas em outro módulo não diretamente relacionado ao primeiro. Imagine que uma alteração no módulo de RH de um sistema ERP gere erros no módulo de faturamento. Situações como essas colocam em cheque a manutenabilidade do sistema e ainda acabam com a confiança dos desenvolvedores em corrigir bugs e desenvolver novas funcionalidades.
</p>
<p align="justify">
	Se componentes internos à um módulo da aplicação não podem ser facilmente componentizados, extraídos e reutilizados, chamamos o código de imóvel. A principal desvantagem da <strong>Imobilidade</strong> é a duplicação de código e a dificuldade de dar manutenção ao sistema, visto que algumas alterações devem ser repetidas em diversos pontos diferentes. Não é incomum esquecer de replicar essas alterações ou correções exatamente na primeira funcionalidade que o usuário utilizará assim que a nova versão do sistema for ao ar.
</p>
<p align="justify">
	Por último, mas não menos importante, temos a <strong>Viscosidade</strong>. Alguns autores separam a viscosidade em duas categorias: Software e ambiente. Ao realizar alterações no software, geralmente nos deparamos com várias formas de implementar o mesmo requisito. Algumas formas preservam a qualidade do código, já outras... bom, para as outras utilizaremos um termo já amplamente conhecido, a gambiarra. Podemos dizer que um sistema possui alta viscosidade do ponto de vista de software quando é mais fácil implementar a gambiarra do que as mudanças necessárias para manter um bom design do código. Do ponto de vista do ambiente,podemos dizer que a viscosidade é alta quando operações rotineiras e necessárias ao processo de desenvolvimento são custosos e geralmente tomam tempo demais do desenvolvedor. Por exemplo: Um commit no sistema de controle de versão ocasiona situação de merge complexa e demorada. Essas situações geralmente estão relacionadas a componentes com multiplas responsabilidades e que possuem alto índice de alteração.
</p>
<p align="justify">
	Não deve ser difícil para desenvolvedores encontrarem exemplos com esses no dia-a-dia. O que pode ser díficil é se livrar deles, mesmo que todos estejam fortemente relacionados a problemas de acoplamento. Há diversos princípios e boas práticas que podem nos ajudar nessa tarefa e em próximos posts nós conheceremos os príncipios <strong>SOLID</strong>, que tem tudo para nos ajudar a nos livrar desses bad smells.
</p>
