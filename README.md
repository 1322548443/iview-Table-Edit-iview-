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

<span class="pl-s1">&lt;/<span class="pl-ent">script</span>&gt;</span></pre></div>
