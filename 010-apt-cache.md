# apt-cache

**Utilizado para manipular e obter informações sobre os pacotes no cache do apt.**

Alguns exemplos:

- `apt-cache pkgnames`: Mostra nome de todos os pacotes no cache.
- `apt-cache stats`: Mostra algumas estatísticas básicas.
- `apt-cache dump`: Mostra um despejo do cache inteiro.
- `apt-cache pkgnames | grep [palavra] | less`:Filtra os resultados da saída que contenham a palavra especificada e faz paginação.
- `apt-cache search [palavra-chave]`: Mostra todos os pacotes relacionados com a palavra chave.
- `apt-cache show [pacote]`: Mostra uma breve descrição sobre um pacote em particular.
- `apt-cache showpkg [pacote]`: Mostra um informação mais geral sobre o pacote.
- `apt-cache depends [pacote]`: Mostra de quais pacotes o pacote especificado depende.