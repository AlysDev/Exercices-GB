import React from "react";
import { render } from "react-dom";
import EXAMPLE_DOCUMENT from "./EXAMPLE_DOCUMENT.json";

class DocumentRenderer extends React.Component {
  render() {
    // The document to render is provided as a prop
    const document = this.props.document;

    return React.createElement(
      "div",
      null,
      React.createElement(
        "p",
        null,
        "The first exercise will ask you to render a document here. ",
        React.createElement("br", null),
        "You can edit the files, and the code in ",
        React.createElement(
          "code",
          null,
          "index.js"
        ),
        ", and the right pane will update automatically ",
        "\u2728",
        "."
      )
    );
  }
}

render(React.createElement(DocumentRenderer, { document: EXAMPLE_DOCUMENT }), document.getElementById("root"));
