- 表单防止刷新事件，出错：不放在上一级div中
```
<form @submit.prevent="myMethod">
    <button type="submit"></button>
</form>

<div @submit.prevent="myMethod">
    <form>
        <button type="submit"></button>
    </form>
</div>
```