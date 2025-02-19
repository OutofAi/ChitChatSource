<p align="center">
  <img src="https://github.com/OutofAi/ChitChatSource/assets/145302363/798510c4-c92f-47f3-8728-738f5b1333bc" alt="logo">
</p>

<table style="border-collapse: collapse; width: 100%;" border="1" align="center">
<tbody>
<tr>
<td style="width: 100%;">GPU variation</td>
</tr>
<tr>
<td style="width: 100%;"><p align="center">
  <img src="https://github.com/OutofAi/ChitChatSource/assets/145302363/08c3d21f-6d70-4e33-a3aa-a4c40a30ae6d" alt="hello world">
</p>
</td>
</tr>
</tbody>
</table>

<p>This is the first part of a collection of templates we are working on for promoting the concept of Model as a Serivce (MaaS). Mainly revolving around using Firebase/Modal/Stripe. One of the user friendliest and cheapest way to deploy your model and creating inference endpoint API is <a href="https://modal.com/">Modal</a>. This example shows the simplicity of deploying Mistral 7B Instruct v0.1 - GGUF with only few lines of code and deploying it on Modal. But you can change it to any model that is supported by LLamacpp</p>
<hr />
<p>Follow us on X for updates regarding the other templates<br /><a href="https://twitter.com/OutofAi">https://twitter.com/OutofAi</a></p>
<p>and also support our channel <br /><a href="https://www.buymeacoffee.com/outofAI">https://www.buymeacoffee.com/outofAI</a></p>
<hr />
<h2 dir="auto" tabindex="-1">Prerequisites</h2>
<p>Make sure you have created an account on <a href="https://modal.com/">Modal.com</a> and install the required Python packages</p>
<pre>pip install modal</pre>
<p>The next command will help you to automatically create a token and set everything up and log you in to simplify deployment</p>
<pre>python3 -m modal setup</pre>
<p>This is all you need to be able to generate an endpoint.</p>
<h2 dir="auto" tabindex="-1">Deploy</h2>
<p>There are two examples avaiable here and depending on cost you can choose which one you like to deploy. We recommend deploying the cpu version first before attempting the gpu one. To deploy the model to create an inference endpoint API you only need to run this command.</p>
<p>CPU version:</p>
<pre>modal deploy chitchat-cpu.py</pre>
<p>GPU version (Running on T4):</p>
<pre>modal deploy chitchat-gpu.py</pre>
<p>After a successful process you will be given entrypoint link in this format</p>
<pre>Created entrypoint: https://[ORG_NAME]--[NAME]-entrypoint.modal.run</pre>
<h2 dir="auto" tabindex="-1">Inference</h2>
<p>We put together a website https://chitchatsource.com/ to simplify and enhance user experience, insert the provided link in previous step on that page to run inference on your model.</p>

<p align="center">
  <img src="https://github.com/OutofAi/ChitChatSource/assets/145302363/79a79b25-5d5b-4e81-b972-b49cc472de66" alt="ChitChat-Settings">
</p>

<p>After saving your deployment link you should be able to run inference on the model. You can use this website for running local FastAPI inference endpoint as well. You just need to make sure the formating and parameters expected matches the one provided in this example. I will do a different repository related to that.</p>

