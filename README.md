<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <script src="https://unpkg.com/gojs/release/go.js"></script>
  <title>Mapa Mental - Características de la Copropiedad</title>
  <style>
    body { font-family: Arial, Helvetica, sans-serif; }
    #myDiagramDiv { width: 100%; height: 500px; }
  </style>
</head>
<body>
  <div id="myDiagramDiv"></div>
  <script>
    function init() {
      var $ = go.GraphObject.make;
      var myDiagram =
        $(go.Diagram, "myDiagramDiv",
          {
            "undoManager.isEnabled": true
          });
          
      // Define the node template
      myDiagram.nodeTemplate =
        $(go.Node, "Auto",
          $(go.TextBlock, { margin: 10 },
            new go.Binding("text", "text"))
        );

      // Create the model data
      var model = $(go.TreeModel);
      model.nodeDataArray =
      [
        { key: "1", text: "Características de la Copropiedad" },
        { key: "2", text: "Pluralidad de Sujetos: dos o más personas" },
        { key: "3", text: "Unidad de Objeto: bien común compartido" },
        { key: "4", text: "Existencia de cuotas ideales: porcentaje de interés" }
      ];
      myDiagram.model = model;
    }
    init();
  </script>
</body>
</html>
