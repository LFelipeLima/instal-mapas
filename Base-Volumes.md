# Documentação

Proposta de estruturação construída e pensada, via este [diagrama](https://github.com/edsongs/instal-mapas/blob/master/Base-Volumes.pdf) de mind-mapping elaborado usando o GitMind, por [Edson Gellert Schubert](http://github.com/edsongs) e [Wiusmarques Moreira](http://github.com/wiusmarques)

**Índice do Documento:**
1. [Manual de Uso](https://github.com/edsongs/instal-mapas/blob/master/Base-Volumes.md#manual-de-uso)
2. [Manual do Administrador](https://github.com/edsongs/instal-mapas/blob/master/Base-Volumes.md#manual-do-administrador)
3. [Manual do Desenvolvedor](https://github.com/edsongs/instal-mapas/blob/master/Base-Volumes.md#manual-do-desenvolvedor)

## Manual de Uso
Este manual é pensado em concentrar todos os documentos necessários para correto uso da plataforma [Mapas Culturais](http://github.com/mapasculturais).

1. Usuário Final
	1. Acesso
		1. Registro Inicial
		2. Confirmação de Registro
		3. Login
	2. Agente
		1. Cadastro
		2. Atualização
		3. Atribuições
	3. Espaço
	4. Projeto
	5. Evento
		1. Criação
	6. Oportunidade
2. Administrador
	1. Evento
		1. Tipo
		2. Anexos
		3. Descrição
	2. Projeto
	3. Oportunidade
		1. Tipos
		2. Formulário
	4. Agente
	5. Registro de Usuário

## Manual do Administrador
Este manual é pensado em concentrar todos os documentos necessários para a administração da plataforma [Mapas Culturais](http://github.com/mapasculturais).

1. [Requisitos de sistema](https://github.com/edsongs/instal-mapas/tree/master/draft/Requisitos%20m%C3%ADnimos).
2. Instalação do Ambiente
	1. Ubuntu/Debian
		1. Deploy
			* [Instalação Manual](https://github.com/edsongs/instal-mapas/tree/master/draft/Deploy/Instala%C3%A7%C3%A3o%20Manual%20Ubuntu%2018.04%20e%2020.04)
			* [Instalação com Docker](https://github.com/edsongs/instal-mapas/tree/master/draft/Deploy/Instala%C3%A7%C3%A3o%20Docker%20Ubuntu%2018.04%20e%2020.04)
		2. Desevolvimento
			* [Instalação Manual]
			* [Instalação com Docker](https://github.com/edsongs/instal-mapas/blob/master/draft/Desenvolvimento/Docker/Docker-UBUNTU20.md)
	2. Fedora/Centos
		1. Deploy
			* [Instalação Manual]
			* [Instalação com Docker]
		2. Desevolvimento
			* [Instalação Manual]
			* [Instalação com Docker](https://github.com/edsongs/instal-mapas/blob/master/draft/Desenvolvimento/Docker/Docker-FEDORA32.md)
3. Migração de Servidor
	1. Registros
		1. Exportação do BD
		2. Importação BD
		3. Uso de API
	2. Temas
		1. Textos
		2. Imagens
		3. Cores

4. Perfil de Usuário
	1. Super Administrador SaaS
	2. Administrador SaaS
	3. Administrador
	4. Usuário

5. Administração do Ambiente
	1. Subsites
		1. Textos
		2. Imagens
		3. Administradores
		4. Tema
			1. Imagens
	2. Segurança
		1. Captcha
		2. Certificado
	3. Plugins
		1. Mailer
		2. Autenticação
			1. Google
			2. Facebook
			3. Twitter
			4. LinkedIn
			5. Local
				* Regras Autenticação
			6. Captcha
		3. Aldir Blanc

# Manual do Desenvolvedor
Este manual é pensado em concentrar todos os documentos necessários para o desenvolvimento/programação da plataforma [Mapas Culturais](http://github.com/mapasculturais).
1. API
	1. Dicionário Funções 
	2. Exemplos de Uso
2. Programação
3. Repositório
4. Extensões
	1. Inclusão de Campos
	2. Alteração de Tema
