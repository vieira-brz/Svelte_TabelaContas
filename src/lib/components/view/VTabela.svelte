<script lang="ts">

    let dados: any[] = [
        {
            id: 0,
            desc: "Teste de item 1",
            valor: 239.9,
            parcelas: 1,
            pago: 0
        },
        {
            id: 1,
            desc: "Teste de item 2",
            valor: 300,
            parcelas: 2,
            pago: 1
        }
    ];

</script>

<div class="content-table">

    <div class="actions">
        <div class="add-item">
            <div class="input-field">
                <input 
                id="desc"
                autofocus
                type="text" 
                placeholder="Digite a descrição da conta..."
                />
                <label for="desc">Descrição</label>
            </div>

            <div class="input-field">
                <input 
                id="valor"
                step=".01"
                type="number"
                placeholder="R$ 0,00"
                />
                <label for="valor">Valor</label>
            </div>

            <button 
                type="submit"
                id="adicionar"
            >
                Adicionar
            </button>
        </div>
    </div>

    <hr>

    <table>
        <thead>
            <th>#</th>
            <th>Descrição</th>
            <th>Valor</th>
            <th>Parcelas</th>
            <th>Pago</th>
        </thead>
        <tbody>
            {#each dados as dado (dado.id)}
                <tr>
                    <td>{ dado.id }</td>
                    <td>{ dado.desc }</td>
                    <td>{ dado.valor }</td>
                    <td>{ dado.parcelas }</td>
                    <td>{ dado.pago }</td>
                </tr>
            {/each}
        </tbody>
    </table>

</div>

<style>
    table {
        width: 100%;
        border: 1px solid;
        white-space: nowrap;
        border-collapse: collapse;
    }

    table thead th {
        border-bottom: 1px solid;    
    }

    table thead th,
    table tbody tr td {
        padding: 15px;
        border-right: 1px solid;
    }
</style>