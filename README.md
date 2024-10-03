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
<p>95100</p>

<pre>
    db.funcionarios.aggregate([
    {
        $match: { "cargo": /vendas/i }
    },
    {
        $group: {
            _id: null,
            gasto_em_salario: { $sum: "$salario" }
        }
    }
])
</pre>

<br><br>
        
<h3>7. Um novo departamento foi criado. O departamento de Inovações. Ele será locado no Brasil. Por favor, adicione-o no banco de dados da empresa colocando quaisquer informações que você achar relevantes.
<p></p>

<pre>
    db.departamentos.insertOne({
    "_id": ObjectId("85992103f9b3e0b3b3c1fe74"),
    "nome": "Inovações",
    "escritorio": ObjectId("5f8b3f3f9b3e0b3b3c1e3e3e")
});
</pre>
    
<br><br>
            
<h3>8. O departamento de Inovações está sem funcionários. Inclua alguns colegas de turma nesse departamento.  
<p></p>

<pre>
    db.funcionarios.insertMany([
    {
        "nome": "Grazielly Oliveira",
        "telefone": "(11) 9564-4353",
        "email": "grazyoli@gmail.com",
        "dataAdmissao": "2003-06-21",
        "cargo": "Analista de Banco de Dados",
        "salario": 17000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947'),
    },
    {
        "nome": "Mariana Paiva",
        "telefone": "(11) 94080-2315",
        "email": "maripaiva@gmail.com",
        "dataAdmissao": "2015-03-06",
        "cargo": "Desenvolvedora Back-End",
        "salario": 13000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947')
    },
    {
        "nome": "Danilo Alcantara",
        "telefone": "(11) 99653-5332",
        "email": "daniloalcantara@gmail.com",
        "dataAdmissao": "2012-02-10",
        "cargo": "Scrum Master",
        "salario": 15000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947'),
    },
    {
        "nome": "Gustavo Rocha Cunha",
        "telefone": "(11) 93085-3174",
        "email": "gucunha@gmail.com",
        "dataAdmissao": "2022-08-13",
        "cargo": "Desenvolvedor Full Stack",
        "salario": 15000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947'),
    },
    {
        "nome": "Iury Sven de Oliveira",
        "telefone":  "(11) 98305-7222",
        "email": "iurysven@gmail.com",
        "dataAdmissao": "2019-05-18",
        "cargo": "Desenvolvedor Front End",
        "salario": 13000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947'),
    },
    {
        "nome": "Kawan Barbosa Turchiai",
        "telefone": "(11) 91116-1868",
        "email": "kawant@gmail.com",
        "dataAdmissao": "2020-03-20",
        "cargo": "Desenvolvedor Front End",
        "salario": 13000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947')
    }, 
    {
        "nome": "Celio Amorim",
        "telefone": "(11) 92226-1868",
        "email": "celioa@gmail.com",
        "dataAdmissao": "2020-03-20",
        "cargo": "Desenvolvedor Front End",
        "salario": 13000,
        "departamento": ObjectId('66f1c0efd15d5494e3f31947')
    }
]);
</pre>
        
<br><br>
                
<h3>9. Quantos funcionarios a empresa Momento tem agora?
<p>31 funcionários.</p>

<pre>db.funcionarios.countDocuments()</pre>
    
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
        
        
