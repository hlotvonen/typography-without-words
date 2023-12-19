<script>

  let firstHeader = {
    position: "left",
    marginTop: "marginBottom-0",
    marginBottom: "marginBottom-0",
  };
  let secondParagraph = {
    indent: "indent",
    marginTop: "marginBottom-0",
  };
  let secondHeader = {
    show: false,
    position: "left",
  };
  let thirdHeader = {
    show: false,
    position: "left",
  };
</script>

<main>

  <article>
    <div>
      <p class={firstHeader.marginTop}>
          xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
      </p>
      <h1 class="{firstHeader.position}  {firstHeader.marginBottom}">
        {#if firstHeader.position == "outside" || firstHeader.position == "inside" }
          oooo<br/>
          ooo
        {:else}
          ooooo
        {/if}
      </h1>


      {#if thirdHeader.show === true}
        <h1 class="{thirdHeader.position}">
          {#if thirdHeader.position == "outside" || thirdHeader.position == "inside" }
            oooo<br/>
            ooo
          {:else}
            ooooo
          {/if}
        </h1>
      {/if}


      <p class="{secondParagraph.marginTop}">
        {#if firstHeader.position == "inside" }
          xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
        {:else}
          xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
        {/if}
      </p>

      {#if secondHeader.show === true}
        <h1 class="{secondHeader.position}">
          {#if secondHeader.position == "outside" || secondHeader.position == "inside" }
            oooo<br/>
            ooo
          {:else}
            ooooo
          {/if}
        </h1>      
      {/if}

      <p class="{secondParagraph.indent}"> 
        xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
      </p>

    </div>
  </article>

  <aside>

    <details open>
      <summary>Heading #1</summary>
      <div>
        <h2>Position</h2>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"left"}>
          Left
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"center"}>
          Center
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"right"}>
          Right
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"outdent"}>
          Outdented
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"indent"}>
          Indented
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"outside"}>
          Outside
        </label>
        <label>
          <input type=radio bind:group={firstHeader.position} value={"inside"}>
          Inside
        </label>
      </div>

      <div>
        <h2>Space before</h2>
        <label>
          <input type=radio bind:group={firstHeader.marginTop} value={"marginBottom-0"}>
          0
        </label>
        <label>
          <input type=radio bind:group={firstHeader.marginTop} value={"marginBottom-1"}>
          1
        </label>
        <label>
          <input type=radio bind:group={firstHeader.marginTop} value={"marginBottom-2"}>
          2
        </label>
      </div>

      <div>
        <h2>Space after</h2>
        <label>
          <input type=radio bind:group={firstHeader.marginBottom} value={"marginBottom-0"}>
          0
        </label>
        <label>
          <input type=radio bind:group={firstHeader.marginBottom} value={"marginBottom-1"}>
          1
        </label>
        <label>
          <input type=radio bind:group={firstHeader.marginBottom} value={"marginBottom-2"}>
          2
        </label>
      </div>
    </details>

    <details>
      <summary>Heading #2</summary>
      <div>
        <label>
          <input type=checkbox bind:checked={secondHeader.show}>
            Show
        </label>
      </div>
      <div>
        <h2>Heading position</h2>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"left"}>
          Left
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"center"}>
          Center
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"right"}>
          Right
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"outdent"}>
          Outdented
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"indent"}>
          Indented
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"outside"}>
          Outside
        </label>
        <label>
          <input type=radio bind:group={secondHeader.position} value={"inside"}>
          Inside
        </label>
      </div>
    </details>  

    <details>
      <summary>Paragraph #2</summary>
      <div>
        <h2>Space before</h2>
        <label>
          <input type=radio bind:group={secondParagraph.marginTop} value={"marginBottom-0"}>
          0
        </label>
        <label>
          <input type=radio bind:group={secondParagraph.marginTop} value={"marginBottom-1"}>
          1
        </label>    
      </div>

      <div>
        <h2>Indentation</h2>
        <label>
          <input type=radio bind:group={secondParagraph.indent} value={""}>
          No
        </label>
        <label>
          <input type=radio bind:group={secondParagraph.indent} value={"indent"}>
          Yes
        </label>    
      </div>
    </details>

 


    <details>
      <summary>Heading #3</summary>
      <div>
        <label>
          <input type=checkbox bind:checked={thirdHeader.show}>
            Show
        </label>
      </div>
      <div>
        <h2>Heading position</h2>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"left"}>
          Left
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"center"}>
          Center
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"right"}>
          Right
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"outdent"}>
          Outdented
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"indent"}>
          Indented
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"outside"}>
          Outside
        </label>
        <label>
          <input type=radio bind:group={thirdHeader.position} value={"inside"}>
          Inside
        </label>
      </div>
    </details>  

  </aside>
</main>



<style>
  main {
    display:grid;
    grid-template-columns: 3fr 1fr;
    height: 100%;
    width: 100%;
  }
	article {
		font-family: monospace;
		font-size: 2em;
    line-height: 1.1;
    display: flex;
    justify-content: center;
    padding-top:5rem;
    word-break: break-all;
	}
  article > div {
    max-width: 330px;
    word-wrap: break-word;
  }
  aside {
    border-left:1px solid #000;
    overflow: auto;
    padding-bottom:100%;
  }
  aside h2 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
  }
  aside details {
    padding:0.5rem;
    border-bottom: 1px solid black;
  }
  aside summary {
    font-variant: small-caps;
    text-transform: lowercase;
  }
  aside label {
    display: block;
  }
  aside div {
    margin-top:1rem;
  }

  /*
  Otsikon paikka
  */
  .left {
    text-align: left;
  }
  .center {
    text-align: center;
  }
  .right {
    text-align: right;
  }
  .outdent {
    margin-left:-2ch;
  }
  .indent {
    text-indent:2ch;
  }
  .outside {
    text-align: right;
    height: 0;
    transform: translateX(calc(-100% - 1ch));
  }
  .inside {
    float:left;
    padding-right: 1ch;
  }
  /*
  Otsikon marginaalit
  */
  .marginBottom-0 {
    margin-bottom:0rem;
  }
  .marginBottom-1 {
    margin-bottom:1ex;
  }
  .marginBottom-2 {
    margin-bottom:2ex;
  }
  .marginTop-0 {
    margin-top:0rem;
  }
  .marginTop-1 {
    margin-top:1rem;
  }


</style>