# Include-Header-Fotter-HTML-JavaScript
Make header and footer files to be included in multiple html pages

Create header.html and footer.html

Include in HTML Pages:
  <div data-include="header"></div>
  <div data-include="footer"></div>

Add java script at the end of the page:
    $(function(){
    var includes = $('[data-include]');
    jQuery.each(includes, function(){
      var file = $(this).data('include') + '.html';
      $(this).load(file);
    });
    });
