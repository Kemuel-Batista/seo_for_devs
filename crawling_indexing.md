- 3 Estágios do Google

Como trabalham os robôs e algoritmos do Google

01 - Crawling

Crawler/Spider = Rastejar, rastejador, rastejando pela teia (web) para encontrar os sites
Finalizando a etapa 01 que é encontrar o site pela essa imensidão de conteúdo segue-se para etapa 02

02 - Indexing

Observar o conteúdo do site, titulo, elementos de imagens, vídeos, se é duplicado de outra página da internet, caso seja duplicado de outro lugar, o robô sempre vai dar preferência para a página original
O algoritmo de indexação fala que não é toda página que passou pelo Crawling que vai ser indexada. É observada toda qualidade da página, se a página está com carregamento lento.

03 - Serving

Entregar a página/site para usuário o que ele buscou.

---

- Rendering (Processo de interpretação e transformação do JS para o HTML)

Interpretação como se fosse o browser
Pode demorar dias ou semanas

---

- URL (Melhores práticas)

1. Uniform Resource Locator (Localizador de recurso único)
Recurso? Página HTML, Arquivo JavaScript, Imagem, Vídeo
E sempre será encontrado esse recurso atráves de um link

- RCF 3986 (https://www.rfc-editor.org/rfc/rfc3986)
- Não podem conter caracteres especiais e nem espaço (serão convertidas em um formato ASCII válido)

Melhores práticas:
1. Simples e descritiva (https://meusite.com/como-iniciar-em-programacao)
2. Palavras localizadas na URL, se aplicável. (https://meusite.com/br/iniciantes/aprender-programacao)
3. UTF-8 enconding (https://meusite.com/programa%23E78-web) -> programação

Piores práticas
1. Ruim para leitura de um ser humano
2. Non-ASCII caracteres
3. Underscore
4. Palavras juntas

Se é bom para humanos, logo é bom para robôs

Resolvendo problemas comuns

1. Crie uma estrutura de URL Simples
2. Considere usar um arquivo robots.txt para bloquear acesso do Googlebot a URLs problemáticas
  Considere bloquear URLs dinâmicas, como urls que geram resultados de pesquisa, ou espaços infinitos.
3. Sempre que possível, evite o uso de IDs de sessão em URLs.
4. Maiúsculas e Minúsculas
5. Encurte as URLs removendo parâmetros desnecessários
6. Se o seu site tem um calendário infinito, adicione um atributo: no-follow aos links
7. Verifique links quebrados.

---

Certificados SSL

1. Dados encriptados
2. https mais relevante que o http
3. com ou sem www
4. Search Console adicione todas as versões
5. Trabalhe o redirecionamento canônico (301 permanente para não caracterizar conteúdo duplicado)

---

Links 

Utilizado para encontrar uma nova página

Links rastreáveis

1. Apenas <a> com atributo <href>

```
<a href="https://example.com">
<a href="/products/category/shoes">
```

2. Qualidade do texto no link

Texto claro do que a página referência é
Pode usar o atributo title para isso
Se for imagem, o Google irá utilizar o alt da imagem como texto
Simples, conciso, natural

3. Links internos

Referência ao próprio conteúdo
Melhor entendimento do Google em relação ao site como um todo
Ajuda a encontrar outras páginas dentro do seu próprio site
Recomendado ter ao menos 1 link referenciando outra página

4. Links externos

Ajuda a estabelecer confiança
  Geralmente as pessoas irão citar bons sites para seus leitores
  O robô entende que o conteúdo é relevante, pois está citando a fonte

É ótimo para o robô encontrar bons sites
Se você não confia na fonte, use no-follow

4.1 Qualificando os links externos

nofollow, ugc, sponsored são valores para usar no atributo relationship e podem ser utilizados múltiplos, apenas separando por vírgulas

```
<a rel="nofollow" href="https://example.com">
```

---
Sitemap

Um arquivo que lista todas as páginas de um website
Ajuda os mecanismos de busca a encontrar e indexar seu site com maior eficiência