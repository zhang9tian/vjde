Just  a  Development Environment  for VIM . (VJDE) 
And now , It's support C++/C by ctags 
(VIM>=700  , +ruby future is on , JDK 1.5 support , JDK1.4 (maybe, not tested)) 

It's Had  been tested on Leopard 10.5.1 . 

use <c-space> as the Code completion key! 
change it by 
:let g:vjde_completion_key='<c-space>' 


English Version will coming soon. 
Just work for : 
       Project manager (load/store  your VJDE settings) 
       Code completion ( working for java and jsp,taglib,html,xml,xsl,xsd) (VIM 7.0 required) 
       Source tools( variable extract local, member,argument,  extract number or String to constance , fix build 
                             unreported exception error ( depends on getqflist() ) 
        Source tools ( Override methods, implements interface,extract import, sort import) 
       Create javadoc (depends on jcommentor.vim) 
       Create getter/setter stub. 
       Generate constructor of class which has all member; 
(2009-04-03 
      Support for annotation completion. 
New(2005-09-08) 
       Use readtags for tags parse. 
       Bug fix. 
New(2005-09-02) 
       Code completion for more language available .(require ctags) 
       let g:vjde_ctags_exts='vim;rb' 
       Code template more powerfull! 
      Put your own definition file , such as c.iab,vim.iab,cpp.iab ruby.iab to ~/.vim/vjde/ 
       let g:vjde_iab_exts='c;vim;cpp;rb' 
      in you c/c++/vim/ruby file, you can use <c-j> 
       
New(2005-09-01) 
       More beautiful document viewer. ^_^ 
       C++/C Code completion support for both GUI and Console 
       C++/C parameter information support for both GUI and Console 
       use: 
       ctags --c++-kinds=+px -R . 
       For search speed , Befor your use Code completion, 
      use: 
       :call VjdeCppGenerateIdx() 
      to generate a index file for your every tag file. 
      see vcde.txt for detail 
New (2005-08-27) 
       Add JAVA document preview in GUI mode 
       Add code template like (for block...) in console mode. 
       Improved Preview window. 
New (2005-09-01) 
        More beautiful document window.^_^ 
        C++/C preview support 
       C++/C parameter information support. 

New (2005-08-22) 
         Add import statement for classes . 
         Add code template like (for block, while block...) 
         Create javadoc (depends on jcommentor.vim) 
         Create getter/setter stub. 
         Generate constructor of class which has all member; 
         Allow    write your own template file in: ~/vim/.vjde/iab.vjde 
                                see vimfile/plugin/vjde/tlds/iab.vjde for detail. 
         Bugfix for vim install on a folder like : c:\program files\vim.. 
         Add menu shortcut. 
New (2005-04-30) Add sensitive java code support for dot '.' , '@', 
       Add sensitive Jsp code support for '<' ':' and space. 
New . Code completion support for packages. 
         import java.net.<CTR>-x<CTR>-u 

         or in coding: 
               java.io.<CTR>-x<CTR>-u 

        Code completion       
This future is depends on JDK, the java reflect API. 
               available for 
                System.<CTR>-x<CTR>-u 
                System.o<CTR>-x<CTR>-u 
                System.out.<CTR>-x<CTR>-u 
             
               a[+-*/%&|^=] str.<CTR>-x<CTR>-u 
               
               return str.<CTR>-x<CTR>-u 
                 
                new Something(str.<CTR>-x<CTR>-u 
         Use it , enjoy it. 
         Completion for jsp 
                <jsp:<CTR>-x<CTR>-u 
                <jsp:include <CTR>-x<CTR>-u 
                <jsp:include flush="<CTR>-x<CTR>-u 
                <jsp:us<CTR>-x<CTR>-u 
         Completion for taglib (ie. STL) 
           <%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core";;%> 
             :XMLns stl_c c 
             <c:<CTR>-x<CTR>-u 
             <c:out <CTR>-x<CTR>-u 
             ..... 

         Completion for xml ....(See doc for detail...) 


        Definition search ( User Command    :Vjdei) 
                you can list a class or a field or a method detail 
                For example: 
                 System.out.println(str.toUpperCase().tr.... 
                Place cursor on the class System, the detail of System  would be shown , Constructor, fields 
,methods, inner class ... 

             
TODO list : 


Tanks for every one who's name is occurred in my source code. ^_^ 

 
install details
unzip this file 
         tar -xzf vjde.tgz  /usr/share/vim/vimfiles 
         chmod +x /usr/share/vim/vimfiles/plugin/vjde/readtags 

start vim 
          :helptags /usr/share/vim/vimfiles/doc 
          :h vjde 

To use VJDE GUI preview , add the preview.dll of old version for the latest version.