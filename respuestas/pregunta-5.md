MATCH (e:Empresa)
WITH collect(e) AS empresas
MATCH (p:Persona)-[:AMIGO_DE]->(a:Persona)-[:TRABAJA_EN]->(e2:Empresa)
WITH p, collect(DISTINCT e2) AS empresas2, empresas
WHERE empresas2 = empresas
RETURN p.nombre
