# iview-Table-Edit-iview-
实现iview中表格可以编辑组件

<p>main.js</p>


<div class="highlight highlight-text-html-vue">
<pre>
import Vue from 'vue'
import CanEditTable from 'CanEditTable.vue'

Vue.component('CanEditTable', CanEditTable)</pre></div>

<p>demo.vue</p>
 <can-edit-table refs="table1" @on-delete="handleDel" v-model="tableData" :columns-list="columnsList"></can-edit-t
<div class="highlight highlight-text-html-vue"><pre>&lt;<span class="pl-ent">template</span>&gt;
	&lt;<span class="pl-ent">can-edit-table</span> <span class="pl-e">refs</span>=<span class="pl-s1"><span class="pl-pds">'</span>table1<span class="pl-pds">'</span></span> @<span class="pl-e">on-delete</span>=<span class="pl-s1"><span class="pl-pds">'</span><span class="pl-c1">handleDel</span><span class="pl-pds">'</span></span> <span class="pl-e">v-model</span>=<span class="pl-s1"><span class="pl-pds">'</span>tableData</span><span class="pl-pds">'</span></span> :<span class="pl-e">columns-list</span>=<span class="pl-s1"><span class="pl-pds">'</span><span class="pl-s">columns-list</span><span class="pl-pds">'</span></span> </span><span class="pl-pds">'</span></span>&gt;&lt;/<span class="pl-ent">can-edit-table</span>&gt;
&lt;/<span class="pl-ent">template</span>&gt;
<span class="pl-s1">&lt;<span class="pl-ent">script</span>&gt;</span>
<span class="pl-s1"><span class="pl-k">export</span> <span class="pl-c1">default</span>{</span>
<span class="pl-s1">  <span class="pl-en">data</span>(){</span>
<span class="pl-s1">    <span class="pl-k">return</span>{</span>
<span class="pl-s1">      data<span class="pl-k">:</span>{</span>
<span class="pl-s1">        name<span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>Root<span class="pl-pds">'</span></span>,</span>
<span class="pl-s1">        id<span class="pl-k">:</span> <span class="pl-c1">0</span>,</span>
<span class="pl-s1">        children<span class="pl-k">:</span> [</span>
<span class="pl-s1">          {</span>
<span class="pl-s1">            name<span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>Node 1-1<span class="pl-pds">'</span></span>,</span>
<span class="pl-s1">            id<span class="pl-k">:</span> <span class="pl-c1">1</span>,</span>
<span class="pl-s1">            children<span class="pl-k">:</span> [</span>
<span class="pl-s1">              {</span>
<span class="pl-s1">                name<span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>Node 2-1<span class="pl-pds">'</span></span>,</span>
<span class="pl-s1">                id<span class="pl-k">:</span> <span class="pl-c1">2</span></span>
<span class="pl-s1">              }</span>
<span class="pl-s1">            ]</span>
<span class="pl-s1">          },</span>
<span class="pl-s1">          {</span>
<span class="pl-s1">            name<span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>Node 1-2<span class="pl-pds">'</span></span>,</span>
<span class="pl-s1">            id<span class="pl-k">:</span> <span class="pl-c1">3</span></span>
<span class="pl-s1">          }</span>
<span class="pl-s1">        ]</span>
<span class="pl-s1">      }</span>
<span class="pl-s1">    }</span>
<span class="pl-s1">  },</span>
<span class="pl-s1">  methods<span class="pl-k">:</span> {</span>
<span class="pl-s1">    <span class="pl-en">assignData</span>(<span class="pl-smi">data</span>) {</span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> data is a json object that node infomation was exchanged inside.You need to assign to finish the last step of exchange.</span></span>
<span class="pl-s1">      </span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> If you have not use vuex or something similar, you can just assign data to this.data</span></span>
<span class="pl-s1">      <span class="pl-c1">this</span>.<span class="pl-c1">data</span> <span class="pl-k">=</span> data</span>
<span class="pl-s1">      </span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> If you have used vuex or something similar, you need to write assign code by yourselft.</span></span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> vuex as an example:</span></span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> updateData function is a mutation of vuex. </span></span>
<span class="pl-s1">      </span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> this.updateData(data)</span></span>
<span class="pl-s1">    },</span>
<span class="pl-s1">    <span class="pl-en">curNodeClicked</span>(<span class="pl-smi">model</span>,<span class="pl-smi">component</span>) {</span>
<span class="pl-s1">      <span class="pl-c"><span class="pl-c">//</span> information of the node clicked just now.</span></span>
<span class="pl-s1">    },</span>
<span class="pl-s1">  }</span>
<span class="pl-s1">}</span>
<span class="pl-s1">&lt;/<span class="pl-ent">script</span>&gt;</span></pre></div>
