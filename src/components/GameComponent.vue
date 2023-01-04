<template>
   <div class="fields">
        <div class="field field-1" @click="markPosition1()"><span>{{ fields.pos1 }}</span></div>
        <div class="field field-2" @click="markPosition2()"><span>{{ fields.pos2 }}</span></div>
        <div class="field field-3" @click="markPosition3()"><span>{{ fields.pos3 }}</span></div>
        <div class="field field-4" @click="markPosition4()"><span>{{ fields.pos4 }}</span></div>
        <div class="field field-5" @click="markPosition5()"><span>{{ fields.pos5 }}</span></div>
        <div class="field field-6" @click="markPosition6()"><span>{{ fields.pos6 }}</span></div>
        <div class="field field-7" @click="markPosition7()"><span>{{ fields.pos7 }}</span></div>
        <div class="field field-8" @click="markPosition8()"><span>{{ fields.pos8 }}</span></div>
        <div class="field field-9" @click="markPosition9()"><span>{{ fields.pos9 }}</span></div>
   </div>
</template>

<script>
export default {
    name: 'GameComponent',

    data() {
        return {
            fields: {
                pos1: null,
                pos2: null,
                pos3: null,
                pos4: null,
                pos5: null,
                pos6: null,
                pos7: null,
                pos8: null,
                pos9: null,
            },

            currentPlayer: 'o', //o is player1, x is player2
        }
    },

    methods: {
        changePlayer() {
            if (this.currentPlayer == 'o') {
                this.currentPlayer = 'x';
            } else {
                this.currentPlayer = 'o';
            }
        },

        markPosition1() {
            if (this.fields.pos1 == null) {
                this.fields.pos1 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition2() {
            if (this.fields.pos2 == null) {
                this.fields.pos2 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition3() {
            if (this.fields.pos3 == null) {
                this.fields.pos3 = this.currentPlayer;
                this.changePlayer()
            }
        },

        markPosition4() {
            if (this.fields.pos4 == null) {
                this.fields.pos4 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition5() {
            if (this.fields.pos5 == null) {
                this.fields.pos5 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition6() {
            if (this.fields.pos6 == null) {
                this.fields.pos6 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition7() {
            if (this.fields.pos7 == null) {
                this.fields.pos7 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition8() {
            if (this.fields.pos8 == null) {
                this.fields.pos8 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        markPosition9() {
            if (this.fields.pos9 == null) {
                this.fields.pos9 = this.currentPlayer;
                this.changePlayer();
                this.checkWinner();
            }
        },

        checkWinCompb1() {
            if (this.fields.pos1 == null || this.fields.pos2 == null || this.fields.pos2 == null) {
                return false;
            } else if (this.fields.pos1 == this.fields.pos2 && this.fields.pos2 == this.fields.pos3) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb2() {
            if (this.fields.pos4 == null || this.fields.pos5 == null || this.fields.pos6 == null) {
                return false;
            } else if (this.fields.pos4 == this.fields.pos5 && this.fields.pos5 == this.fields.pos6) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb3() {
            if (this.fields.pos7 == null || this.fields.pos8 == null || this.fields.pos9 == null) {
                return false;
            } else if (this.fields.pos7 == this.fields.pos8 && this.fields.pos8 == this.fields.pos9) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb4() {
            if (this.fields.pos1 == null || this.fields.pos4 == null || this.fields.pos7 == null) {
                return false;
            } else if (this.fields.pos1 == this.fields.pos4 && this.fields.pos4 == this.fields.pos7) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb5() {
            if (this.fields.pos2 == null || this.fields.pos5 == null || this.fields.pos8 == null) {
                return false;
            } else if (this.fields.pos2 == this.fields.pos5 && this.fields.pos5 == this.fields.pos8) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb6() {
            if (this.fields.pos3 == null || this.fields.pos6 == null || this.fields.pos9 == null) {
                return false;
            } else if (this.fields.pos3 == this.fields.pos6 && this.fields.pos6 == this.fields.pos9) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb7() {
            if (this.fields.pos1 == null || this.fields.pos5 == null || this.fields.pos9 == null) {
                return false;
            } else if (this.fields.pos1 == this.fields.pos5 && this.fields.pos5 == this.fields.pos9) {
                return true;
            } else {
                return false;
            }
        },

        checkWinCompb8() {
            if (this.fields.pos3 == null || this.fields.pos5 == null || this.fields.pos7 == null) {
                return false;
            } else if (this.fields.pos4 == this.fields.pos5 && this.fields.pos5 == this.fields.pos6) {
                return true;
            } else {
                return false;
            }
        },

        checkWinner() {
            if(this.checkWinCompb1) {
                alert('WinnerPlayer: 1');
            } else if (this.checkWinCompb2) {
                alert('Winner player: 2');
            } else if (this.checkWinCompb3) {
                alert('Winner player: 3');
            } else if (this.checkWinCompb4) {
                alert('Winner player: 4');
            } else if (this.checkWinCompb5) {
                alert('Winner player: 5');
            } else if (this.checkWinCompb6) {
                alert('Winner player: 6');
            } else if (this.checkWinCompb7) {
                alert('Winner player: 7');
            } else if (this.checkWinCompb8) {
                alert('Winner player: 8');
            }
        },


    },

    mounted() {

    }
}
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Jost:wght@200&display=swap');

    * {
        font-family: 'Jost', sans-serif;
    }

    .fields {
        display: grid;
        grid-template-columns: repeat(3, 100px);
        grid-template-rows: repeat(3, 100px);
        gap: 1px;
    }

    .field {
        display: flex;
        justify-content: center;
        align-items: center;
        background: grey;
    }
    
    .field > span {
        font-size: 120px;      
    }
    
</style>