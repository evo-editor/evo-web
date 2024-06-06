<script>
    import { Icon } from 'svelte-icons-pack'
    import { FaBrandsWindows, FaBrandsApple, FaBrandsLinux, FaSolidDownload } from 'svelte-icons-pack/fa'
</script>


<div class="content">
    <div class="downloads">
        <div class="operating-system" id="windows">
            <Icon src={FaBrandsWindows} size={60} />


            <div class="buttons-wrapper">
                <h3>X64</h3>

                <div>
                    <a href="/bin/evo_1.0.0_x64_en-US.msi" download class="download-button"><Icon src={FaSolidDownload} />MSI</a>
                    <a href="/bin/evo_1.0.0_x64-setup.exe" download class="download-button"><Icon src={FaSolidDownload} />EXE</a>
                </div>
            </div>


            <div class="buttons-wrapper">
                <h3>ARM64</h3>

                <div>
                    <a href="/bin/evo_1.0.0_x64_en-US.msi" download class="download-button"><Icon src={FaSolidDownload} />MSI</a>
                    <a href="/bin/evo_1.0.0_x64-setup.exe" download class="download-button"><Icon src={FaSolidDownload} />EXE</a>
                </div>
            </div>
        </div>


        <div class="operating-system" id="linux">
            <Icon src={FaBrandsLinux} size={60} />

            <div class="buttons-wrapper">
                <h3>X64</h3>

                <div>
                    <a href="/bin/evo_1.0.0_x64_en-US.msi" download class="download-button"><Icon src={FaSolidDownload} />DEB</a>
                    <a href="/bin/evo_1.0.0_x64-setup.exe" download class="download-button"><Icon src={FaSolidDownload} />RPM</a>
                </div>
            </div>


            <div class="buttons-wrapper">
                <h3>ARM32</h3>

                <div>
                    <a href="/bin/evo_1.0.0_x64_en-US.DEB" download class="download-button"><Icon src={FaSolidDownload} />DEB</a>
                    <a href="/bin/evo_1.0.0_x64-setup.RPM" download class="download-button"><Icon src={FaSolidDownload} />RPM</a>
                </div>
            </div>


            <div class="buttons-wrapper">
                <h3>ARM64</h3>

                <div>
                    <a href="/bin/evo_1.0.0_x64_en-US.DEB" download class="download-button"><Icon src={FaSolidDownload} />DEB</a>
                    <a href="/bin/evo_1.0.0_x64-setup.RPM" download class="download-button"><Icon src={FaSolidDownload} />RPM</a>
                </div>
            </div>
        </div>

        <div class="operating-system" id="mac">
            <Icon src={FaBrandsApple} size={60} />
        </div>
    </div>
</div>




<style scoped>
    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 40px;
    }

    .downloads {
        display: flex;
        align-items: start;
        justify-content: center;
        gap: 30px;
    }

    .operating-system {
        width: 300px;
        padding: 15px 10px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        align-items: center;
        background: linear-gradient(55deg, #00f6fd 0%, #00f6fd 15%, #2c52fd 50%, #c217fd 85%, #c217fd 100%);
    }

    :global(.operating-system > svg) {
        margin-bottom: 40px !important;
    }

    .buttons-wrapper {
        margin-top: 10px;
        width: 100%;
        padding: 0 10px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }






    .buttons-wrapper > div {
        flex-grow: 1;
        display: flex;
        align-items: center;
        justify-content: end;
        gap: 8px;
    }


    .download-button {
        background-color: #050130;
        border-radius: 5px;
        padding: 2px 10px;
        font-size: 14px;
        display: flex;
        align-items: center;
        gap: 10px;
        transition: 0.2s;
    }

    .download-button:hover {
        background-color: #0d046d;
        transition: 0.2s;
    }
</style>