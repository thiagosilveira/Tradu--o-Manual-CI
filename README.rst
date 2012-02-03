#####################
Manual do CodeIgniter 
#####################

**********
Instruções
**********

O manual do CodeIgniter usa o Sphinx para gerir a documentacão e os vários
formatos de saída. Páginas são escritas utilizando o formato
`ReStructured Text <http://sphinx.pocoo.org/rest.html>`_.

Pré-requisitos
==============

Sphinx requer Python, que se você estiver no OS X já está instalado.
Você pode confirmar dentro do Terminal executando o comando ``python``
sem nenhum paramêtro. Esta ação deve carregar e informar qual versão
você tem instalada. Se não for 2.7+, instale a 2.7.2 aqui
http://python.org/download/releases/2.7.2/

Instalação
==========

1. Instalar `easy_install <http://peak.telecommunity.com/DevCenter/EasyInstall#installing-easy-install>`_
2. ``easy_install sphinx``
3. ``easy_install sphinxcontrib-phpdomain``
4. Instalar o CI Lexer que permite sintaxe nos códigos para PHP, HTML, CSS, and JavaScript, exemplos (veja *cilexer/README*)
5. ``cd user_guide_src``
6. ``make html``

Editando e Criando Documentação
===============================

Todos os arquivos estão dentro de *source/* e é aqui que você
adiciona nova documentação ou altera a já existente. Assim como
na alteração de códigos, nós recomendamos trabalhar com os branches e
depois fazer um pull request para o branch and is where you will add new
documentation or modify existing documentation.  Just as with code changes,
we recommend working from feature branches and making pull requests to
the *develop* branch of this repo.

Então onde está o HTML?
=======================

Obviously, the HTML documentation is what we care most about, as it is the
primary documentation that our users encounter.  Since revisions to the built
files are not of value, they are not under source control.  This also allows
you to regenerate as necessary if you want to "preview" your work.  Generating
the HTML is very simple.  From the root directory of your user guide repo
fork issue the command you used at the end of the installation instructions::

	make html

You will see it do a whiz-bang compilation, at which point the fully rendered
user guide and images will be in *build/html/*.  After the HTML has been built,
each successive build will only rebuild files that have changed, saving
considerable time.  If for any reason you want to "reset" your build files,
simply delete the *build* folder's contents and rebuild.

***************
Style Guideline
***************

Please refer to source/documentation/index.rst for general guidelines for
using Sphinx to document CodeIgniter.
