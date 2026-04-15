```cypher
// =====================
// NODOS
// =====================

CREATE
// Personas
(p1:Persona {id:1, nombre:"Ana", edad:30}),
(p2:Persona {id:2, nombre:"Luis", edad:35}),
(p3:Persona {id:3, nombre:"Marta", edad:28}),
(p4:Persona {id:4, nombre:"Carlos", edad:40}),
(p5:Persona {id:5, nombre:"Elena", edad:32}),

// Empresas
(e1:Empresa {id:1, nombre:"TechCorp"}),
(e2:Empresa {id:2, nombre:"DataSoft"}),

// Proyectos
(pr1:Proyecto {id:1, nombre:"Apollo"}),
(pr2:Proyecto {id:2, nombre:"Zeus"}),

// Ciudades
(c1:Ciudad {id:1, nombre:"Madrid"}),
(c2:Ciudad {id:2, nombre:"Barcelona"}),

// Universidades
(u1:Universidad {id:1, nombre:"UPM"}),
(u2:Universidad {id:2, nombre:"UB"}),

// Tecnologias
(t1:Tecnologia {id:1, nombre:"Neo4j"}),
(t2:Tecnologia {id:2, nombre:"Python"});

// =====================
// RELACIONES (8 tipos)
// =====================

CREATE
// Sociales
(p1)-[:AMIGO_DE {since:2018}]->(p2),
(p2)-[:AMIGO_DE {since:2019}]->(p3),
(p3)-[:AMIGO_DE {since:2020}]->(p4),
(p4)-[:AMIGO_DE {since:2017}]->(p5),
(p1)-[:AMIGO_DE {since:2021}]->(p3),

// Trabajo
(p1)-[:TRABAJA_EN {rol:"dev"}]->(e1),
(p2)-[:TRABAJA_EN {rol:"analyst"}]->(e1),
(p3)-[:TRABAJA_EN {rol:"manager"}]->(e2),
(p4)-[:TRABAJA_EN {rol:"dev"}]->(e2),

// Proyectos
(p1)-[:PARTICIPA_EN {horas:20}]->(pr1),
(p2)-[:PARTICIPA_EN {horas:15}]->(pr1),
(p3)-[:PARTICIPA_EN {horas:30}]->(pr2),

// Colaboración
(p1)-[:TRABAJA_CON]->(p2),
(p2)-[:TRABAJA_CON]->(p3),
(p3)-[:TRABAJA_CON]->(p4),

// Residencia
(p1)-[:VIVE_EN]->(c1),
(p2)-[:VIVE_EN]->(c1),
(p3)-[:VIVE_EN]->(c2),
(p4)-[:VIVE_EN]->(c2),
(p5)-[:VIVE_EN]->(c1),

// Gestión
(p4)-[:GESTIONA]->(pr2),

// Educación
(p1)-[:ESTUDIO_EN]->(u1),
(p2)-[:ESTUDIO_EN]->(u1),
(p3)-[:ESTUDIO_EN]->(u2),

// Tecnología
(p1)-[:USA_TECNOLOGIA]->(t1),
(p2)-[:USA_TECNOLOGIA]->(t2),
(p3)-[:USA_TECNOLOGIA]->(t1);
```
