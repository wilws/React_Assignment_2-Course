<script>
export default {
    methods:{
        screenRotatedDetector(){
            return this.getWidth() > this.getHeight() ? true : false
            
        },
        getHeight(){
            return window.screen.height;
        },
        getWidth(){
            return window.screen.width;
        }
    }
}
</script>