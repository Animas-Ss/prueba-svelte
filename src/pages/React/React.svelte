<script>
  import GoBack from "../../components/GoBack.svelte";


</script>

<section>
    <div class="bloob"></div>
</section>

<style>
    section{
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: #313131;
    }
    .bloob{
        width: 200px;
        height: 200px;
        background: transparent;
        border: 5px solid #313131;
        border-radius: 42% 56% 72% 28% / 42% 42% 56% 48%;
        box-shadow:
        -6px -6px 10px rgb(10, 10, 10),
        6px 6px 8px rgba(255, 255, 255, 0.5),
        inset -3px -3px 7px rgb(12, 12, 12),
        inset 3px 3px 5px rgba(255, 255, 255, 0.5);
        animation: morph 3.75s linear infinite;
    }

    @keyframes morph{
        0%, 100%{
            border-radius: 42% 56% 72% 28% / 42% 42% 56% 48%;
        }
        33%{
            border-radius: 72% 28% 48% 48% / 28% 28% 72% 72%;
        }
        66%{
            border-radius: 100% 56% 56% 100% / 100% 100% 56% 56%;
        }
    }
</style>