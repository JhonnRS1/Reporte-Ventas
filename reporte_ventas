import openpyxl

# Lista de ventas
ventas = [
    {'fecha': '2024-07-01', 'monto': 1000, 'descripcion': 'Arroz 15kg'},
    {'fecha': '2024-07-02', 'monto': 120, 'descripcion': 'Gasesosa Pepsi 3L'},
    {'fecha': '2024-07-02', 'monto': 400, 'descripcion': 'Ron Cartavio'},
]

def generar_reporte_ventas_excel():
    """
    Genera un reporte de ventas y guarda los datos en un archivo Excel.
    
    :return: None
    """
    # Crear un nuevo libro de trabajo (workbook)
    libro_trabajo = openpyxl.Workbook()
    hoja = libro_trabajo.active
    hoja.title = 'Reporte de Ventas'
    
    # Encabezados de columnas
    hoja['A1'] = 'Fecha'
    hoja['B1'] = 'Monto'
    hoja['C1'] = 'Descripción'
    
    # Llenar el libro con los datos de ventas
    fila = 2
    for venta in ventas:
        hoja[f'A{fila}'] = venta['fecha']
        hoja[f'B{fila}'] = venta['monto']
        hoja[f'C{fila}'] = venta['descripcion']
        fila += 1
    
    # Guardar el libro de trabajo
    nombre_archivo = 'reporte_ventas.xlsx'
    libro_trabajo.save(nombre_archivo)
    
    print(f"Reporte de ventas guardado en {nombre_archivo}")

# Generar y guardar el reporte de ventas en Excel
generar_reporte_ventas_excel()
