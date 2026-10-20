Pour les dependeces : 

# $npm audit : 	n’importe quelle faille existe, même « low »
# --audit-level=moderate	: au moins une faille moderate, high ou critical
# --audit-level=high	: au moins une faille high ou critical
# --audit-level=critical :	uniquement les failles critical


echo $LASTEXITCODE 
(1 echec / 0 succes )

npm test
echo "tests : $LASTEXITCODE"      # attendu : 0

npm audit --audit-level=high
echo "audit : $LASTEXITCODE"      # attendu : 1