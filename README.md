<div class="animategroup">
    <div [class]="selectedType"></div>
    <p-selectButton [options]="types" [(ngModel)]="selectedType"></p-selectButton>
</div>





:host ::ng-deep {
    p-selectButton{
        & .ui-button.ui-button-text-only.ui-state-default.ui-widget.ng-star-inserted{
            width: 100px;
            background-color: rgba($color: #000000, $alpha: 0);
            border-color: red;
            animation:myfirst3 0.5s;
            &.ui-state-active{
                border-color: red;
                animation:myfirst2 0.5s;
            }
        }
    }
}
.animategroup{
    position:relative;
    &>.animater{
        position:absolute; 
        left:100px; 
        width: 100px;
        height: 33px;
        background:#F00;
        animation:myfirst 0.5s;
    }
    &>.animatel{
        position:absolute; 
        left:0px; 
        width: 100px;
        height: 33px;
        background:#F00;
        animation:myfirst1 0.5s;
    }
}
@keyframes myfirst
{
	0% {left:0px;}
	100% {left:100px;}
}
@keyframes myfirst1
{
	0% {left:100px;}
	100% {left:0px;}
}
@keyframes myfirst2
{
	0% {
        border-color:rgba($color: #000000, $alpha: 0);
    }
    99% {
        border-color:rgba($color: #000000, $alpha: 0);
    }
	100% {
        border-color:red;
    }
}
@keyframes myfirst3
{
	0% {
        border-color:rgba($color: #000000, $alpha: 0);
    }
    30% {
        border-color:rgba($color: #000000, $alpha: 0);
    }
	100% {
        border-color:red;
    }
}
