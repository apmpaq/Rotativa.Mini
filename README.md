# Rotativa.Mini 
### v1.0

Rotativa.Mini is a extracted minified version of Rotativa library. It helps you to build pdf file out of html string in any .NET flatform and makes implementation simplier.

### Here's link for rotativa 
https://github.com/webgio/Rotativa


### How to use?
1. Take the output file for Rotativa.Mini.dll and add referance in your project.
2. Add Rotativa Exe File into your project


           var rotativaPath = @"C:\Users\siraj\source\repos\Rotativa.Mini\Rotativa.Mini.Demo\Rotativa";
            var style = @"C:\Users\siraj\source\repos\Rotativa.Mini\Rotativa.Mini.Demo\Stylesheet1.css";

            var fileHtml = File.ReadAllText(@"C:\Users\siraj\source\repos\Rotativa.Mini\Rotativa.Mini.Demo\dddd.html");

            var options =
              new RotativaMiniOptions()
               .SetWindowStatusIdentifier("ready_to_print")
               .SetCopies(2)
               .SetPageSize(Size.A4)
               .SetStyleSheet(style)
               .SetFooter(@"C:\Users\siraj\source\repos\Rotativa.Mini\Rotativa.Mini.Demo\ddFooter.html")
               .SetPageMargins(1, 1, 5, 1);

            var pdfData = RotativaMiniConverter.ConvertHtml(rotativaPath, options, fileHtml);

            File.WriteAllBytes("Test.pdf", pdfData);


You can little work arround to support all the path as relative path
