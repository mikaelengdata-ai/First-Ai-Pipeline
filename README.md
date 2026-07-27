# Dados B2B brutos recebidos pela esteira
empresas_registradas = [
    {"nome": "TechCorp", "usuarios": 150, "status": "ativo"},
    {"nome": "DevStudio", "usuarios": 8, "status": "inativo"},
    {"nome": "MegaRetail", "usuarios": 1200, "status": "ativo"},
]

# Processamento automatizado: filtra apenas grandes contas ativas
clientes_validos = [
    empresa for empresa in empresas_registradas 
    if empresa["usuarios"] >= 100 and empresa["status"] == "ativo"
]

# Exibe o resultado final estruturado
print("--- RELATÓRIO DE DADOS B2B ---")
for cliente in clientes_validos:
    print(f"Empresa: {cliente['nome']} | Licenças Ativas: {cliente['usuarios']}")
    
