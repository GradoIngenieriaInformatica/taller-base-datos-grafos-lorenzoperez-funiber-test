MATCH (p:Persona)-[:TRABAJA_EN]->(e)
MATCH (p)-[:VIVE_EN]->(c)
RETURN p, e, c
