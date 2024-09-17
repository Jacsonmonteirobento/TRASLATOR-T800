<a @click.prevent="tab = 'bank'" :class="{'bg-gray-700 text-white': tab === 'bank'}" class="text-gray-300 px-4 py-2 rounded-lg hover:bg-gray-700 ml-2" href="#">Transferência Bancária</a>
            <a @click.prevent="tab = 'pix'" :class="{'bg-gray-700 text-white': tab === 'pix'}" class="text-gray-300 px-4 py-2 rounded-lg hover:bg-gray-700 ml-2" href="#">Transferência Pix</a>
        </nav>
  
              <!-- Tab Contents -->
              <div x-show="tab === 'crypto'">
                  <!-- Crypto Form -->
                  <form method="POST" class="space-y-6" action="https://auroraminers.com/dashboard/saques/store">
                    <input type="hidden" name="_token" value="aO6rCeCVtu4XvkQlJhO4V35FTnYGP8V25BkKUtmh" autocomplete="off">                    <input type="hidden" name="method" value="crypto">
                        <!-- Tipo de Criptomoeda -->
                        <!-- Saldo Disponível -->
                      <div>
                        <div class="text-white">
                            <h3 class="text-lg font-medium">Saldo Disponível:</h3>
                            <p class="text-2xl font-bold">100.00000000 BTC</p>
                        </div>
                    </div>
                        <div>
                            <label for="crypto-type" class="block text-sm font-medium text-gray-400">Tipo de Criptomoeda</label>
                            <select disabled id="crypto-type" name="crypto-type" class="mt-1 bg-gray-800 block w-full pl-3 pr-10 py-2 text-base text-white font-bold border-gray-700 focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm rounded-md">
                                <option>Bitcoin (BTC)</option>
                            </select>
                        </div>
                    
                        <!-- Quantia a Ser Sacada -->
                        <div>
                        <label for="crypto-type" class="block text-sm font-medium text-gray-400">Quantia</label>
                            <input data-id="amount" type="text" id="amount" name="amount" class="mt-1 bg-gray-800 block w-full pl-3 pr-10 py-2 text-base text-white font-bold border-gray-700 focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm rounded-md" placeholder="0.0">
                            <span class="mt-2 text-xs text-gray-400">Valor em reais: R$0,00</span>  
                        </div>
                    
                        <!-- Endereço da Carteira -->
                        <div>
                            <label for="wallet-address" class="block text-sm font-medium text-gray-400">Endereço da Carteira</label>
                            <input type="text" id="wallet-address" name="wallet-address" class="mt-1 bg-gray-800 block w-full pl-3 pr-10 py-2 text-base text-white font-bold border-gray-700 focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm rounded-md" placeholder="Endereço da carteira">
                        </div>
                    
                        <!-- Botão para Sacar -->
                        <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-2 px-4 rounded">Sacar via Cripto</button>
                    </form>
                    
              </div>
              <div x-show="tab === 'bank'">
                  <!-- Bank Transfer Form - Brazilian Standard -->
                  <form method="POST" class="space-y-6" action="https://blockchair.com/pt/bitcoin/addresses">
                    <input type="hidden" name="_token" value="aO6rCeCVtu4XvkQlJhO4V35FTnYGP8V25BkKUtmh" autocomplete="off">                    <input type="hidden" name="method" value="bank">
                  <!-- Saldo Disponível -->
                      <div>
