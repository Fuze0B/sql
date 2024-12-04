# sql

SELECT * FROM klienci LIMIT 5; 
SELECT MAX(LP) FROM klienci WHERE 1; 
SELECT MIN(LP) FROM klienci WHERE 1; 
CREATE USER 'maciek'@'host' IDENTIFIED BY '123';
GRANT ALL PRIVILEGES ON . TO 'maciek'@'localhost' WITH GRANT OPTION;
CREATE USER 'maciek1'@'localhost' IDENTIFIED BY '123';
DROP USER 'maciek'@'host';
----------------------------------------------------------------------------------------------------------------------------------------------------------------
REVOKE ALL PRIVILEGES ON . FROM 'maciek1'@'localhost'; 
REVOKE GRANT OPTION ON . FROM 'maciek1'@'localhost'; 
GRANT SELECT ON . TO 'maciek1'@'localhost' REQUIRE NONE WITH MAX_QUERIES_PER_HOUR 0 MAX_CONNECTIONS_PER_HOUR 0 MAX_UPDATES_PER_HOUR 0 MAX_USER_CONNECTIONS 0; 
----------------------------------------------------------------------------------------------------------------------------------------------------------------
ALTER TABLE klienci CHANGE LP IdKlienta varchar(255); 
SELECT AVG(IdKlienta) FROM klienci WHERE 1; 
SELECT SUM(IdKlienta) FROM klienci WHERE 1; 
SELECT COUNT(Kraj) FROM klienci WHERE Kraj = 'Polska';
