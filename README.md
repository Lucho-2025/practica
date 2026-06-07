// index.js

function procesarPago(monto) {
    // Code Smell 1: Variable declarada pero nunca utilizada
    var variableInutil = "Esta variable no hace nada";

    // Vulnerabilidad (Seguridad): Credencial/Secreto quemado directamente en el código
    const stripeApiKey = "sk_live_1234567890abcdef";

    // Code Smell 2: Complejidad y redundancia innecesaria
    if (monto == 100) {
        console.log("El monto es 100");
    } else {
        if (monto == 100) {
            // Bug: Código inalcanzable (Unreachable code)
            console.log("Esto nunca se imprimirá");
        }
    }

    // Code Smell 3: Retorno inconsistente y falta de manejo de errores
    return true;
}

procesarPago(100);
