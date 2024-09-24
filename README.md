<h1>Análise da Empresa Momento</h1>

<p>Contém a base de indicados da empresa "Momento" para treinar consultas complexas no MongoDB.</p>
    
<h3>1. Quantos funcionarios da empresa Momento trabalham no departamento de vendas?</h3>

<p>- Tem 8 consultores de vendas</p>
<pre>db.funcionarios.countDocuments({cargo:"Consultor de Vendas"});</pre>

<p>- Tem 1 para vendas</p>
<pre>db.funcionarios.countDocuments({cargo:"Vendas"});</pre>

<p>- Tem 1 Representante de Vendas para a América Latina</p>
db.funcionarios.countDocuments({cargo:"Representante de Vendas para a América Latina"});

<br><br>

<h3>2. Inclua suas próprias informações no departamento de Tecnologia da empresa.</h3>

<pre>db.funcionarios.insertOne({"_id": ObjectId, "nome": "Heloisa Mendes", "telefone": "453.345.1233", "cargo": "Desenvolvedora Mobile", "salario": 12000, "comissao": true, "departamento": "Tecnologia"});</pre>
<pre>
  _id: Code('function(t){return(0,A.assertArgsDefinedType)([t],[[void 0,"string","number","object"]],"ObjectId"),new e.ObjectId(t)}'),
  nome: 'Heloisa Mendes',
  telefone: '453.345.1233',
  cargo: 'Desenvolvedora Mobile',
  salario: 12000,
  comissao: true,
  departamento: 'Tecnologia'
</pre>

<br><br>
        
<h3>3. Agora diga, quantos funcionários temos ao total na empresa?</h3>
<p>24 funcionários.</p>

<pre>db.funcionarios.countDocuments()</pre>

<br><br>
        
<h3>4. E quanto ao Departamento de Tecnologia?</h3>
<p>2 pessoas do departamento de Tecnologia</p>

<pre>db.departamentos.countDocuments({nome: "Tecnologia"});</pre>

<br><br>
        
<h3>5. Qual a média salarial do departamento de tecnologia?</h3>
<p>O departamento de Tecnologia de Web Developer tem a média salárial de: 3.475</p>

<pre>{cargo:"Web Developer"}</pre>

<br><br>
        
<h3>6. Quanto o departamento de Vendas gasta em salários?</h3>
<p></p>

<pre></pre>

<br><br>
        
<h3>7. Um novo departamento foi criado. O departamento de Inovações. Ele será locado no Brasil. Por favor, adicione-o no banco de dados da empresa colocando quaisquer informações que você achar relevantes.
<p></p>

<pre></pre>
    
<br><br>
            
<h3>8. O departamento de Inovações está sem funcionários. Inclua alguns colegas de turma nesse departamento.  
<p></p>

<pre></pre>
        
<br><br>
                
<h3>9. Quantos funcionarios a empresa Momento tem agora?
<p></p>

<pre></pre>
    
<br><br>
            
<h3>10. Quantos funcionários da empresa Momento possuem conjuges?
<p></p>

<pre></pre>
    
<br><br>
            
<h3>11. Qual a média salarial dos funcionários da empresa Momento, excluindo-se o CEO?
<p></p>

<pre></pre>
    
<br><br>
            
<h3>12. Qual a média salarial do departamento de tecnologia? 
<p></p>

<pre></pre>

<br><br>
            
<h3>13. Qual o departamento com a maior média salarial?
<p></p>

<pre></pre>
    
<br><br>
            
<h3>14. O departamento com o menor número de funcionários?</h3>
<p></p>

<pre></pre>

<br><br>
        
<h3>15. Pensando na relação quantidade e valor unitario, qual o produto mais valioso da empresa?</h3>
<p></p>

<pre></pre>

<br><br>
        
<h3>16. O produto mais vendido da empresa?</h3>
<p></p>

<pre></pre>

<br><br>
        
<h3>17. O produto menos vendido da empresa?</h3>
<p></p>

<pre></pre>

<br><br>
        
        
