# IIS

## Gerenciamento

- O app de gerencia é o Internet Infomation Services (IIS) Manager;
- O caminho do site web padrão é o **c:\inetpub\wwwroot**;
- Portanto o IIS cria automaticamente um Web Site Padrão com as extensões do servidor instaladas no diretório c:\inetpu\wwwroot
- É possível alterar esse diretório base;

## Criando diretórios virtuais

- Ao criar suas novas páginas Web você pode colocá-las no diretório d:\inetpub\wwwroot ou em um de seus subdiretórios.
- Na criação do diretório virtual será necessário definir o alias e o caminho do diretório onde o site será armazenado.
- Será necessário definir permissões de acesso, nesse caso defina permissões de leitura, execução de scripts e gravação.

Observações:
- Um diretório virtual representa um diretório físico na web e não precisa usar o mesmo nome que o diretório físico.
- Um diretório virtual não precisa ser necessariamente um subdiretório de  d:\inetpub\wwwroot.
	- Assim você pode criar o diretório c:\sites_web dando a ele o nome de diretório virtual - Sites. Para acessar o seu site bastaria informar http://localhost/Sites

Quando você cria um diretório virtual com o IIS ele também é marcado como um aplicativo Web, com isto os arquivos ASP.NET nesse diretório serão executados por si próprios , usarão o seu próprio conjunto de dados de sessão local e terão os seus próprios ajustes de configuração.

# Referências

[Instalando e configurando o Internet Information Services (IIS)](http://www.macoratti.net/vbn_iis.htm)