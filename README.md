Used Awesome-CV template for building my resume. 

<h1 align="center">
  <a href="https://github.com/posquit0/Awesome-CV" title="AwesomeCV Documentation">
    <img alt="AwesomeCV" src="https://github.com/posquit0/Awesome-CV/raw/master/icon.png" width="200px" height="200px" />
  </a>
  <br />
  Awesome CV
</h1>
showdown.extension('targetlink', function() {
  return [{
    type: 'lang',
    regex: /\[((?:\[[^\]]*]|[^\[\]])*)]\([ \t]*<?(.*?(?:\(.*?\).*?)?)>?[ \t]*((['"])(.*?)\4[ \t]*)?\)\{\:target=(["'])(.*)\6}/g,
    replace: function(wholematch, linkText, url, a, b, title, c, target) {

      var result = '<a href="' + url + '"';

      if (typeof title != 'undefined' && title !== '' && title !== null) {
        title = title.replace(/"/g, '&quot;');
        title = showdown.helper.escapeCharacters(title, '*_', false);
        result += ' title="' + title + '"';
      }

      if (typeof target != 'undefined' && target !== '' && target !== null) {
        result += ' target="' + target + '"';
      }

      result += '>' + linkText + '</a>';
      return result;
    }
  }];
});
For downloading my resume, please click [here](https://aekhz.com/Resume_AnkitKhare.pdf){:target="_blank"}
