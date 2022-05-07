import XLSX from "/dist/xlsx.full.min.js"

var reader = new FileReader()
reader.onload = function (e) {
    var data = e.target.result
    var workbook = XLSX.read(data, { type: 'binary' })
    let sheetName = workbook.SheetNames[0]
    let worksheet = workbook.Sheets[sheetName]
    let rowObject = XLSX.utils.sheet_to_row_object_array(worksheet)
    const finalJsonData = JSON.stringify(rowObject, undefined, 5)
    console.log(finalJsonData)
}

reader.readAsBinaryString(this.excelFile)