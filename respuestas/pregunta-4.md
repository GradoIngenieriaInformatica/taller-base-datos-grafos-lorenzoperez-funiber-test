MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad)
RETURN c.nombre
