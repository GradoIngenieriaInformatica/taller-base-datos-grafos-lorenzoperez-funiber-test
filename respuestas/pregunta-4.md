MATCH (p:Persona)-[:USA_TECNOLOGIA]->(t:Tecnologia)
WITH p, collect(t) AS techs
WHERE size(techs) > 1
RETURN p.nombre, techs
