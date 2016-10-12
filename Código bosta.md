Public Class Compras
    Private Sub SalvarToolStripMenuItem_Click(sender As Object, e As EventArgs) Handles SalvarToolStripMenuItem.Click
        If Cliente_ComboBox.Text <> "" Then



            Panel1.Visible = True
            Valor_Pago_TextBox.Focus()


            '  Form2.Show()
            ' Me.Close()
        Else
            MsgBox("Selecione um cliente!")
        End If

    End Sub

    Private Sub Compra_BindingNavigatorSaveItem_Click(sender As Object, e As EventArgs) Handles Compra_BindingNavigatorSaveItem.Click
        Me.Validate()
        Me.Compra_BindingSource.EndEdit()
        Me.TableAdapterManager.UpdateAll(Me.BancodedadosDataSet)

    End Sub

    Private Sub Compras_Load(sender As Object, e As EventArgs) Handles MyBase.Load

        'TODO: This line of code loads data into the 'BancodedadosDataSet.Clientes' table. You can move, or remove it, as needed.
        Me.ClientesTableAdapter.Fill(Me.BancodedadosDataSet.Clientes)
        'TODO: This line of code loads data into the 'BancodedadosDataSet._Produtos_' table. You can move, or remove it, as needed.
        Me.Produtos_TableAdapter.Fill(Me.BancodedadosDataSet._Produtos_)
        'TODO: This line of code loads data into the 'BancodedadosDataSet._Compra_' table. You can move, or remove it, as needed.
        Me.Compra_TableAdapter.Fill(Me.BancodedadosDataSet._Compra_)

        Me.Compra_BindingSource.AddNew()
        txtCusto.Text = "00,00"

        '----------------------------------------
        'Dim Valor As Double = txtvalkg.Text
        '----------------------------------------



    End Sub


    Private Sub cbID_SelectedIndexChanged(sender As Object, e As EventArgs) Handles cbID.SelectedIndexChanged
        'Dim Val As Double
        'Val = txtvalkg.Text


        If cbID.Text = "0" Then
            txtProdutos.Text = "Ferro"
            txtvalkg.Text = "0,15"

        End If
        If cbID.Text = "1" Then
            txtProdutos.Text = "Papelão"
            txtvalkg.Text = "0,20"
        End If

        If cbID.Text = "2" Then
            txtProdutos.Text = "Pet"
            txtvalkg.Text = "0,70"
        End If

        If cbID.Text = "3" Then
            txtProdutos.Text = "Plástico"
            txtvalkg.Text = "0,50"
        End If

        If cbID.Text = "4" Then
            txtProdutos.Text = "Plástico Misto"
            txtvalkg.Text = "0,20"
        End If


        If cbID.Text = "5" Then
            txtProdutos.Text = "Filme Branco"
            txtvalkg.Text = "0,10"
        End If

        If cbID.Text = "6" Then
            txtProdutos.Text = "Lata"
            txtvalkg.Text = "2,50"
        End If

        If cbID.Text = "7" Then
            txtProdutos.Text = "Alumínio"
            txtvalkg.Text = "2,50"
        End If

        If cbID.Text = "8" Then
            txtProdutos.Text = "Metal"
            txtvalkg.Text = "5,00"
        End If

        If cbID.Text = "9" Then
            txtProdutos.Text = "Cobre de 2ª"
            txtvalkg.Text = "9,00"
        End If

        If cbID.Text = "10" Then
            txtProdutos.Text = "Bloco"
            txtvalkg.Text = "1,30"
        End If

        If cbID.Text = "11" Then
            txtProdutos.Text = "Motor"
            txtvalkg.Text = "5,00"
        End If

        If cbID.Text = "12" Then
            txtProdutos.Text = "Litro"
            txtvalkg.Text = "0,02"
        End If

        If cbID.Text = "13" Then
            txtProdutos.Text = "Litro de 51"
            txtvalkg.Text = "0,10"
        End If

        If cbID.Text = "14" Then
            txtProdutos.Text = "Garrafao"
            txtvalkg.Text = "0,20"
        End If

        If cbID.Text = "15" Then
            txtProdutos.Text = "Bateria de Carro"
            txtvalkg.Text = "10,00"
        End If

        If cbID.Text = "16" Then
            txtProdutos.Text = "Bateria de Moto"
            txtvalkg.Text = "0,60"
        End If

        If cbID.Text = "17" Then
            txtProdutos.Text = "Caco"
            txtvalkg.Text = "0,02"
        End If

        If cbID.Text = "18" Then
            txtProdutos.Text = "Casco Ambev"
            txtvalkg.Text = "0,10"
        End If

        If cbID.Text = "19" Then
            txtProdutos.Text = "Chumbo"
            txtvalkg.Text = "1,00"
        End If

        If cbID.Text = "20" Then
            txtProdutos.Text = "PVC"
            txtvalkg.Text = "0,03"
        End If

        If cbID.Text = "21" Then
            txtProdutos.Text = "Inox"
            txtvalkg.Text = "1,00"
        End If

        If cbID.Text = "22" Then
            txtProdutos.Text = "Livro"
            txtvalkg.Text = "0,05"
        End If

        If cbID.Text = "23" Then
            txtProdutos.Text = "Papel Branco"
            txtvalkg.Text = "0,05"
        End If

        If cbID.Text = "24" Then
            txtProdutos.Text = "Papel Misto"
            txtvalkg.Text = "0,05"
        End If

        If cbID.Text = "25" Then
            txtProdutos.Text = "Revista"
            txtvalkg.Text = "0,05"
        End If

        If cbID.Text = "26" Then
            txtProdutos.Text = "Placa"
            txtvalkg.Text = "2,00"
        End If

        If cbID.Text = "27" Then
            txtProdutos.Text = "Antimônio"
            txtvalkg.Text = "1,00"
        End If

        If cbID.Text = "28" Then
            txtProdutos.Text = "Radiador"
            txtvalkg.Text = "2,50"
        End If

        If cbID.Text = "29" Then
            txtProdutos.Text = "Óleo Vegetal"
            txtvalkg.Text = "0,10"
        End If

        If cbID.Text = "30" Then
            txtProdutos.Text = "Parachoque"
            txtvalkg.Text = "0,10"
        End If

        If cbID.Text = "31" Then
            txtProdutos.Text = "Cobre com capa"
            txtvalkg.Text = "2,50"
        End If
        If cbID.Text = "32" Then
            txtProdutos.Text = "Radiador A-C"
            txtvalkg.Text = "3,50"
        End If

        If cbID.Text = "33" Then
            txtProdutos.Text = "Persiana"
            txtvalkg.Text = "1,00"
        End If
        If cbID.Text = "34" Then
            txtProdutos.Text = "Placa de PC"
            txtvalkg.Text = "2,00"
        End If

        If cbID.Text = "35" Then
            txtProdutos.Text = "Plástico Paulo"
            txtvalkg.Text = "0,60"
        End If
        If cbID.Text = "36" Then
            txtProdutos.Text = "Filme Colorido"
            txtvalkg.Text = "0,10"
        End If
        If cbID.Text = "37" Then
            txtProdutos.Text = "Cobre de 1ª"
            txtvalkg.Text = "10,00"
        End If
        If cbID.Text = "38" Then
            txtProdutos.Text = "Papelão"
            txtvalkg.Text = "00,18"
        End If

        '--- Não alterar abaixo
        txtQuantidade.Focus()
    End Sub

    Private Sub Lançar_Click(sender As Object, e As EventArgs) Handles Lançar.Click
        Dim Preço, Custo As Double
        Custo = txtCusto.Text
        Preço = txtTotal.Text
        txtCusto.Text = (Custo + Preço)
        Itens.Items.Add(txtProdutos.Text + "     " + txtQuantidade.Text + "X" + txtvalkg.Text + "  =  " + txtTotal.Text)
        Itens_Vendidos_TextBox.Text = (Itens_Vendidos_TextBox.Text + "
  " + txtProdutos.Text + "     " + txtQuantidade.Text + "X" + txtvalkg.Text + "  =  " + txtTotal.Text)

        Peso_Prod.Text = (Peso_Prod.Text + "
" + txtQuantidade.Text)

        Custo_Prod.Text = (Custo_Prod.Text + "
" + lbTotal.Text)

        txtQuantidade.Text = "0"

        Me.Produtos_TableAdapter.Fill(Me.BancodedadosDataSet._Produtos_)
        cbID.Text = ""
        txtQuantidade.Text = "0"
        txtProdutos.Text = ""
        txtvalkg.Text = "0"
        cbID.Focus()



    End Sub

    Private Sub txtTotal_TextChanged(sender As Object, e As EventArgs) Handles txtTotal.TextChanged

    End Sub

    Private Sub Label2_Click(sender As Object, e As EventArgs) Handles Label2.Click

    End Sub

    Private Sub Label1_Click(sender As Object, e As EventArgs) Handles Label1.Click

    End Sub

    Private Sub txtQuantidade_TextChanged(sender As Object, e As EventArgs) Handles txtQuantidade.TextChanged
        If txtvalkg.Text = "" Then
            txtvalkg.Text = "0"
        End If
        If txtQuantidade.Text = "" Then
            txtQuantidade.Text = "0"
        End If
        Dim Quantidade, Valor As Double
        Quantidade = txtQuantidade.Text
        Valor = txtvalkg.Text




        If Quantidade > 0 Then
            lbTotal.Text = Quantidade * Valor
            txtTotal.Text = ("R$ " + lbTotal.Text)

        End If

    End Sub

    Private Sub Cliente_ComboBox_SelectedIndexChanged(sender As Object, e As EventArgs)

    End Sub

    Private Sub CancelarToolStripMenuItem_Click(sender As Object, e As EventArgs) Handles CancelarToolStripMenuItem.Click
        Me.Compra_BindingSource.AddNew()

    End Sub

    Private Sub FecharToolStripMenuItem1_Click(sender As Object, e As EventArgs) Handles FecharToolStripMenuItem1.Click
        Me.Close()
    End Sub

    Private Sub Timer1_Tick(sender As Object, e As EventArgs) Handles Timer1.Tick
        LabelHora.Text = Now
        Data_Label1.Text = LabelHora.Text

    End Sub

    Private Sub Valor_Pago_TextBox_TextChanged(sender As Object, e As EventArgs) Handles Valor_Pago_TextBox.TextChanged
        Dim ValortPago, Total As Double
        ValortPago = Valor_Pago_TextBox.Text
        Total = txtCusto.Text
        If Valor_Pago_TextBox.Text = "" Then
            Valor_Pago_TextBox.Text = "0"
        End If
        If ValortPago > 0 Then
            Diferença_TextBox.Text = (ValortPago - Total)

        End If
    End Sub

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        Me.Validate()
        Me.Compra_BindingSource.EndEdit()
        Me.TableAdapterManager.UpdateAll(Me.BancodedadosDataSet)
        'TODO: This line of code loads data into the 'BancodedadosDataSet.Clientes' table. You can move, or remove it, as needed.
        ' Me.ClientesTableAdapter.Fill(Me.BancodedadosDataSet.Clientes)
        'TODO: This line of code loads data into the 'BancodedadosDataSet._Produtos_' table. You can move, or remove it, as needed.
        '  Me.Produtos_TableAdapter.Fill(Me.BancodedadosDataSet._Produtos_)
        'TODO: This line of code loads data into the 'BancodedadosDataSet._Compra_' table. You can move, or remove it, as needed.
        '  Me.Compra_TableAdapter.Fill(Me.BancodedadosDataSet._Compra_)
        '  Me.Compra_BindingSource.AddNew()

        Form2.Show()
        Imprimir.Show()
        Me.Close()

    End Sub

    Private Sub Cliente_Combobox_SelectedIndexChanged_1(sender As Object, e As EventArgs) Handles Cliente_Combobox.SelectedIndexChanged
        If Cliente_Combobox.Text <> "" Then
            Cliente_TextBox.Text = Cliente_Combobox.Text
        End If
    End Sub

    Private Sub Cliente_TextBox_Click(sender As Object, e As EventArgs) Handles Cliente_TextBox.Click
        Cliente_TextBox.ReadOnly = False

    End Sub

    Private Sub Cliente_TextBox_TextChanged(sender As Object, e As EventArgs) Handles Cliente_TextBox.TextChanged

    End Sub

    Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click
        Panel1.Visible = False

    End Sub

    Private Sub Button3_Click(sender As Object, e As EventArgs) Handles Button3.Click
        Dim Preço, Custo As Double
        Custo = txtCusto.Text
        Preço = txtTotal.Text
        txtCusto.Text = (Custo - Preço)
        Itens.Items.Add("REMOVIDO " + txtProdutos.Text + "     " + txtQuantidade.Text + "X" + txtvalkg.Text + "  =  " + txtTotal.Text)
        Itens_Vendidos_TextBox.Text = (Itens_Vendidos_TextBox.Text + "
  " + txtProdutos.Text + "     " + txtQuantidade.Text + "X" + txtvalkg.Text + "  =  " + txtTotal.Text)

        Peso_Prod.Text = (Peso_Prod.Text + "
" + txtQuantidade.Text)

        Custo_Prod.Text = (Custo_Prod.Text + "
" + lbTotal.Text)

        txtQuantidade.Text = "0"

        Me.Produtos_TableAdapter.Fill(Me.BancodedadosDataSet._Produtos_)
        cbID.Text = ""
        txtQuantidade.Text = "0"
        txtProdutos.Text = ""
        txtvalkg.Text = "0"
        cbID.Focus()
    End Sub
End Class
