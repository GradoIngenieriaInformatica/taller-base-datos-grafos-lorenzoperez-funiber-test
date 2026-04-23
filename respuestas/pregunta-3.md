MATCH (u:Universidad)<-[:ESTUDIA_EN]-(p:Persona)
WITH u, count(p) AS total
WHERE total > 1
RETURN u.nombre, total
